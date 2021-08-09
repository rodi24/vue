<template>
<div id="app">
   <v-app>
    
    <h3>{{source.feed}}</h3>
    <h2>{{name}} settings are :</h2>
    <h3 v-for="(s,index) in seetings" :key="index">
        {{s}}
    </h3>

    <v-text-field
            v-for="(s,index) in detail" :key="index"
            v-model="detail[index]"
            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            
            :type="show1 ? 'text' : 'password'"
            name="input-10-1"
            label="Normal with hint text"
            counter
            @click:append="show1[index] = !show1[index]"
    ></v-text-field> 
    


    <v-btn  
      class="primary"
      @click="OnClick"
    >
      Primary
    </v-btn>
    </v-app>
    
 </div>   

</template>



<script>
export default{
    name: 'SourceList',
    data(){
        return{
            show1: [false,false, false]
        }
    },

    props:{
        source:{},
        seetings: [],
        name: '',
        onClick: Function,
        detail: {},
        
     
    },

    

    methods:{
        OnClick(){
            this.onClick();
            
            //console.log("click from SourceList");
        }
    }
}
</script>

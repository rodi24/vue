<template>
 <div>
  
  <SourceList 
  name="Location" 
  :source="source" 
  :seetings="locationSeetings" 
  :onClick="onClick"
  :detail="locationDetail"
  
  
  >
  </SourceList>

  <SourceList 
  name="Feed" 
  :source="source" 
  :seetings="feedSeetings" 
  :onClick="onClick"
  :detail="feedDetail"
  >
  </SourceList>
  
</div>
</template>

<script>
import SourceList from "./components/SourceList.vue"
export default {
  name: 'App',

  data(){
    return {
      source:{
        location: "FTP Location",
        feed: "TMS Feed",
      },
      locationSeetings:[ "LocationName", "LocationPlace"],
      feedSeetings: ["feedName", "FeedPlace"],
      labellocation: "location",
      labelFeed: "Feed",

      locationDetail:{
        name: "Location Name",
        type: "Location Type",
        password: '123',
      },

      feedDetail:{
        name: "Feed Name",
        type: "Feed Type",
        password: '123',
      },
      
    

    }
  
  }, 
  components:{
      SourceList
  },

  methods:{
    onClick(){
      console.log("clicked from App");
    }
  },


  
};
</script>

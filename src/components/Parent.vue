<template>
  <v-card width="500px">
    <v-card-title>
      {{title}}
    </v-card-title>
    <v-card-text>
      {{content}}
    </v-card-text>
    <v-card-actions>
      <child :id="id" @clicked="OnClicked"/>
    </v-card-actions>
    </v-card>
</template>


<script>
import Child from './Child.vue'
export default {
  props: {
    id: String,
    title: String,
    content: String
  },
  components: {
    Child
  },
  data(){
    return {
    }
  },
  methods: {
    OnClicked(value){
     console.log(value)
    }
  }
}
</script>
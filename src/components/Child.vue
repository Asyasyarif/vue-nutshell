<template>
  <div>
      <v-btn variant="tonal" @click="onSubmit()">
        Submit
      </v-btn>
  </div>
</template>


<script>
export default {
  props: {
    id: String
  },
  data(){
    return {

    }
  },
  methods: {
    onSubmit(){
      this.$emit('clicked', this.id)
    }
  }
}
</script>
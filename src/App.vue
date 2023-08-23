// https://jsonplaceholder.typicode.com/guide/
//  1. Fetch Data GET
//  2. Fetch Data POST
//  3. Fetch Data PUT
//  4. Fetch Data DELETE

<template>
    <h1>Hello World</h1>
</template>

<script>
  import axios from 'axios'
  export default {
      data() {
        return {

        }
      },
      methods: {
        postData(){
          var body = {
            title: 'foo',
            body: 'bar',
            userId: 1,
          }

          var header = {
            'Content-type': 'application/json; charset=UTF-8'
          }

          let res = axios.post('https://jsonplaceholder.typicode.com/posts',
            body,
           {
             headers: {
              header
             }
          })
          console.log(res)

        },
        updateData(){
          var body = {
            title: 'foo',
            body: 'bar',
            userId: 1,
          }

          var header = {
            'Content-type': 'application/json; charset=UTF-8'
          }

          let res = axios.put('https://jsonplaceholder.typicode.com/posts/1',
            body,
           {
             headers: {
              header
             }
          })
          console.log(res)

        },
        deleteData(){
          var header = {
            'Content-type': 'application/json; charset=UTF-8'
          }

          let res = axios.delete('https://jsonplaceholder.typicode.com/posts/1',
           {
             headers: {
              header
             }
          })
          console.log(res)
        }
      },
      mounted(){

      }
  }
</script>

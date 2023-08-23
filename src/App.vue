
//  1. life cycle created, mounted, watch, computed.
//  2. create parent component
//  3. create child component
//  4. communicate beetween component

<template>
      <h1>
       Count : {{counter}}
      </h1>
      <br>
    <v-row>
      <v-col cols="12">
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
          <router-link to="/contact">Contact</router-link>
        </li>
        <li>
          <router-link to="/about">About</router-link>
        </li>
      </ul>
      </v-col>

      <router-view></router-view>
    </v-row>
</template>

<script>
  export default {
    data() {
      return {
          show: true,
          counter: 0
      }
    },
    methods: {
      startCounter(){
        setTimeout(() => {
          this.counter += 1
          this.startCounter()
        }, 1000)
      }
    },
    mounted(){
      this.startCounter()
    }
  }
</script>

<style>
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333333;
  }

  li {
    float: left;
  }

  li a {
    display: block;
    color: white;
    text-align: center;
    padding: 16px;
    text-decoration: none;
  }

  li a:hover {
    background-color: #111111;
  }
</style>
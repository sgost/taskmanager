<template>
  <div>
    <!-- <h1>I know what to do</h1>
    <h1>{{data}}</h1> -->
    <!-- <button v-on:click="hello('Hello man')">Call Hello Function</button> -->

    <!-- <h1>Conditional rendering</h1>
    <h1 v-if="show">show</h1>
    <h1 v-else>Now show</h1>
    <button v-on:click="display">Set show false</button>

    <h1>Conditional rendering</h1>
    <h1 v-if="man">show</h1>
    <h1 v-else>Now show</h1>
    <button v-on:click="display2((this.man = !this.man))">
      Set show false
    </button> -->

    <table border="1px">
      <tr>
        <td>Ids</td>
         <td>Names</td>
      </tr>
      <tr v-for="item in users" :key="item.id">
           <td>{{item.id}}</td>
        <td>{{item.name}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    data: String,
  },
  // methods:{
  //     hello(data)
  //     {
  //         alert(data)
  //     }
  // }
  //   data() {
  //     return { show: true, man: true };
  //   },
  //   methods: {
  //     display() {
  //       this.show = !this.show;
  //     },
  //   },

  data() {
    return {
      users: [
        { id: 1, name: "manoj" },
        { id: 1, name: "tony" },
        { id: 1, name: "guru" },
        { id: 1, name: "vasu" },
      ],
    };
  },
};
</script>
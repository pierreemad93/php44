<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <h1 v-bind:class="[statusClass ,statusClassD ]">{{textname}}</h1>
    <h1 v-bind:class="isSoldOut ? 'danger' : 'success'">{{soldout}}</h1>
    <button v-bind:disabled="isDisabled ">Click me</button>
    <button v-if="disableButton">Click me</button>
    <button v-show="disableButton">Click me</button> -->
    <!-- <h2 v-if="role == 'admin'">Hello Admin</h2>
    <h2 v-else-if="role == 'moderator'">Hello moderator</h2>
    <h2 v-else>Hello user</h2>
    <h2 v-for="name in names" v-bind:key="name">{{name}}</h2>
    <p v-for="info in infos" v-bind:key="info">{{info.id}} {{info.username}} {{info.email}}</p> -->
   <pre>
     {{JSON.stringify(formValue)}}
   </pre>
    <div class="contianer">
      <form>
        <div class="mb-3">
          <label for="exampleInputEmail1" class="form-label">Email address</label>
          <input type="email" class="form-control" v-model="formValue.email">
        </div>
        <div class="mb-3">
          <label for="exampleInputPassword1" class="form-label">Password</label>
          <input type="password" class="form-control" v-model="formValue.password">
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>

  </div>
</template>

<script>
  // import HelloWorld from './components/HelloWorld.vue'

  export default {
    name: 'App',
    // components: {
    //   HelloWorld
    // },
    data() {
      return {
        textname: "Hello From First Vue Page",
        isDisabled: true,
        statusClass: "test",
        statusClassD: "test-two",
        soldout: "Instock",
        isSoldOut: false,
        status: "success",
        disableButton: false,
        role: "moderator",
        names: ['AMIT', 'Pierre', 'test', 'Omar'],
        infos: [{
            id: 1,
            username: "Amit",
            email: "amit@info.com"
          },
          {
            id: 2,
            username: "Pierre",
            email: "pierre@info.com"
          }
        ], 
        formValue:{
          email : '' ,
          password : '' ,
        }
      }
    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  .test {
    background-color: #f00;
    color: #fff;
    font-size: 25px;
  }

  .test-two {
    border: 2px solid #000;
    text-decoration: underline;
  }

  .danger {
    color: #f00
  }

  .success {
    color: #0f0;
  }
</style>
<template>
  <div class="Navbar">
  <nav class="nav">
    <ul>
      <li><router-link :to="'/'">Home</router-link></li>
      <li><a href="#">Services</a></li>
      <li><router-link :to="'/about'">about</router-link></li>
      <li><router-link :to="'/contact'">contact</router-link></li>
      <li  v-for="(id,index) in userIds" :key="index">
        <router-link :to="{name: 'profile',params: {user_id: id}  }">Profile | {{ id }}</router-link>
      </li>
    </ul>
  </nav>
  <div>
  <button @click="contact">Contact Page</button>
  <button @click="about">About Page</button>
  </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data(){
    return {
      userIds: [
        1,2,3,4,5,6,7,8,9
      ]

    }
  },
  methods: {
    about(){
      this.$router.push({name: 'About'})
    },
    contact(){
      this.$router.push({name: 'Contact'})
    }
  }
}

</script>

<style scoped>
.nav{
  text-align: center;

}
.nav ul{
  padding: 0;
}
.nav li{
  display: inline-block;
  margin: 5px;
  padding: 8px;
}


</style>

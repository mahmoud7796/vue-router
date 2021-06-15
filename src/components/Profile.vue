<template>
  <div class="profile">
    <h2>{{ profile }} | ({{UserId}}) </h2>
  </div>
</template>

<script>
export default {
  name: 'profile',
  data () {
    return {
      profile: 'Welcome to profile is page',
      UserId: this.$route.params.user_id
    }
  },
  methods:{
    updateId(){
      this.UserId = this.$route.params.user_id
    },

  },
  watch:{
    $route: 'updateId'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  color: darkred;
}
</style>

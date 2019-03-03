<template>
    <div>
        <h1>Vue Router Demo App</h1>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <router-link class='nav-link' v-for="(data,index) in routes" :key='index' v-bind:to = "data.path">{{data.name}}</router-link>
        </nav>
        <div class="container">
            <router-view></router-view>
        </div>
    </div>
</template>

<script>

export default{
   name:'App',
   data() {
    return {
      routes: this.$router.options.routes
    };
  }
   
}
</script>
<style scoped>
    .nav-item{
        margin:5px;
    }
</style>


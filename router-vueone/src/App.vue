

<template>
  <div class="container mx-auto">
   <p> <router-link to="/">Home</router-link>

     <router-link class="ml-4" to="/about">About</router-link>
   </p>

    <router-view></router-view>
</div>

</template>
<script>export default {
  components: {}
}
</script>
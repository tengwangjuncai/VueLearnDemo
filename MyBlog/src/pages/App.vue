<template>
  <div>
   <div class="app"></div>
    <!--<keep-alive>-->
      <!--<router-view v-if="$route.meta.keepAlive">-->
      <!--</router-view>-->
    <!--</keep-alive>-->

    <!--<router-view v-if="!$route.meta.keepAlive">-->
    <!--</router-view>-->
  </div>

</template>

<script>
    export default {
        name: "App"
    }
</script>

<style>

  body{
     margin: 0;
   }

  .app{
    width: 100vw;
    height: 100px;
    background-color: red;
  }

</style>

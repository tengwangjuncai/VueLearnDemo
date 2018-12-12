<template>
    <div class="home">
      <div class="homeLeft">
        <div class="homeLeft_content">
          <img src=""/>
          <div class="homeLeft_name">藤王俊采</div>
          <div class="homeLeft_sign"></div>
          <div class="homeLeft_line"></div>
          <div class="homeLeft_introduce"></div>
          <div class="homeLeft_pageList">
            <div class="homeLeft_pageItem" v-for=""></div>
          </div>
          <div class="homeLeft_contactPages">
            <div class="homeLeft_page"></div>
          </div>
    </div>
      </div>
      <div class="homeRight"></div>
    </div>
</template>

<script>
    export default {
        name: "HomeView"
    }
</script>

<style scoped>

  .home {

    margin: 0 0;
    padding: 0 0;
    /*清除浮动*/
    overflow: hidden;
    display: flex;
    height: 100%;
    width: 100%;

  }
  .homeLeft{
     margin: 0 0;
     padding: 0 0;
     height: 100vw;
     width: 100vw;
     background-color: darkgreen;
  }
  .homeRight{

    width: 0px;
    height: 100%;
    background-color: red;
  }

</style>

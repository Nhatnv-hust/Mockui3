<template>
  <div id="app">
    <Navigations/>
    <div class="app__routerview">
      <SideBar/>
      <Content class="app__content"/>
    </div>
  </div>
</template>

<script>
import Navigations from './components/Navigations.vue';
import SideBar from './components/SideBar.vue';
import Content from './components/Content.vue';



export default {
  name: 'App',
  components: {
    Navigations,
    SideBar,
    Content
}
}
</script>

<style scoped>
@font-face {
  font-family: NotoSansJP;
  src: url(../src/assets/NotoSansJP-Regular.otf);

   font-family: NotoSans;
  src: url(../src/assets/NotoSansJP-Bold.otf);
}
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: 'NotoSansJP';
  font-size: 12px;
  font-weight: 400;
}
.app__routerview{
  display: flex;
  justify-content: start;


}
.app__content{
  width: 100%;
}
</style>

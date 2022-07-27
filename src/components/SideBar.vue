<template>
  <div class="SideBar__container">
    <div
      class="SideBar__container__img"
      v-for="modul in moduls"
      :key="modul.id"
    >
      <img :src="modul.img" alt="" class="SideBar__container__img" />
    </div>
    <div class="SideBar__container__icon">
      <img :src="imgArow" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      moduls: [
        {
          id: 1,
          img: require("../assets/House.svg"),
        },
        {
          id: 2,
          img: require("../assets/Newspaper.svg"),
        },
        {
          id: 3,
          img: require("../assets/UserCircle.svg"),
        },
        {
          id: 4,
          img: require("../assets/advanced_search.svg"),
        },
        {
          id: 5,
          img: require("../assets/MegaphoneSimple.svg"),
        },
        {
          id: 6,
          img: require("../assets/pocket-2.svg"),
        },
        {
          id: 7,
          img: require("../assets/Group8770.svg"),
        },
        {
          id: 8,
          img: require("../assets/Group484089.svg"),
        },
        {
          id: 9,
          img: require("../assets/Line.svg"),
        },
      ],
      imgArow: require("../assets/ArrowCircleLeft.svg"),
    };
  },
};
</script>

<style scoped lang="scss">
.SideBar__container {
  position: relative;
  z-index: 1;
  top: 64px;
  left: 0;
  width: 72px;
  padding: 40px 18px 0px 18px;
  border-right: 1px solid #dcdcdc;
  .SideBar__container__img {
    //   margin-bottom: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 30px;
    cursor: pointer;
  }
  .SideBar__container__icon {
    margin-top: 190px;
  }
}
@media screen and (max-width:414px){
.SideBar__container{
   display:none;
}
}
</style>
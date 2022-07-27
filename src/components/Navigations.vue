<template>
  <div class="navigations__container">
    <div class="navigations__search">
      <img :src="imgLogo" alt="" />
      <div class="navigation__search__main">
        <i class="fa-solid fa-magnifying-glass"></i>
        <input type="text" :placeholder="this.search.placehoder" />
      </div>
    </div>
    <div class="navigations__profiles">
      <div class="navigations__profiles__info">
        <img :src="this.profile.imgInfo" alt="" />
      </div>
      <div class="navigations__profiles__tag">
        <img :src="this.profile.imgTag" alt="" />
      </div>
      <div class="navigations__profiles__company">
        <img :src="this.profile.imglogoCompany" alt="" />
      </div>
      <div class="border"></div>
      <div class="navigations__profiles__name">{{ this.profile.name }}</div>
      <div class="navigations__profiles__avatar">
        <img :src="this.profile.imgAvatar" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navigations-pages",
  data() {
    return {
      imgLogo: require("../assets/wsp_01.svg"),
      search: {
        imgSearch: require("../assets/Path.svg"),
        placehoder: "メンバーを検索",
      },
      profile: {
        imgInfo: require("../assets/Frame7557.svg"),
        imgTag: require("../assets/Frame7088.svg"),
        imglogoCompany: require("../assets/Frame7556.svg"),
        name: "石原 由梨",
        imgAvatar: require("../assets/avatar.svg"),
      },
    };
  },
};
</script>

<style scopde lang="scss">
$font-stack: "Roboto", sans-serif;
$primary-color: #f5f5f5;
$background-color: #ffffff;

.navigations__container {
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 64px;
  position: absolute;
  z-index: 1;
  margin: 12px 0px;
  box-shadow: 0px 1px 1px $primary-color;
}
.navigations__search {
  display: flex;
  justify-content: start;
  align-items: center;

  img {
    margin: 0px 12px;
  }
  .navigation__search__main {
    width: 320px;
    background-color: #f4f7fb;
    border-radius: 27px;

    i {
      margin: 11px 13px;
    }
    input {
      width: 80%;
      border: none;
      outline: none;
      background-color: #f4f7fb;
    }
  }
}
.navigations__profiles {
  display: flex;
  justify-content: start;
  align-items: center;
  .navigations__profiles__info {
    margin-right: 16px;
  }
  .navigations__profiles__company {
    margin: 0px 24px;
  }
  .border {
    height: 90%;
    width: 5px;
    background-color: #dcdcdc;
  }
  .navigations__profiles__name {
    margin-left: 24px;
    margin-right: 6px;
  }
  .navigations__profiles__avatar {
    margin-right: 24px;
    img {
      border-radius: 20px;
    }
  }
}
</style>
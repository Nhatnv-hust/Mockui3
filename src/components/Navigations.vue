<template>
  <div class="navigations__container">
    <div class="navigations__search">
      <img :src="imgLogo" alt="" />
      <div class="navigations__search__do">
        <div class="navigation__search__main">
          <img src="../assets/search.svg" alt="" />
          <input type="text" :placeholder="this.search.placehoder" />
        </div>
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
  position: fixed;
  z-index: 10;
  margin: 12px 0px;
  box-shadow: 0px 1px 1px $primary-color;
  background-color: #ffffff;
}
.navigations__search {
  display: flex;
  justify-content: start;
  align-items: center;

  img {
    margin: 0px 12px;
    cursor: pointer;
  }
  .navigation__search__main {
    display: flex;
    align-items: center;
    width: 320px;
    height: 40px;
    background-color: #f4f7fb;
    border-radius: 27px;

    img {
      cursor: pointer;
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
  cursor: pointer;
  .navigations__profiles__info {
    margin-right: 16px;
  }
  .navigations__profiles__company {
    margin: 0px 24px;
  }
  .navigations__profiles__company::after {
    position: absolute;
    content: "";
    background-color: #dcdcdc;
    top: 6px;
    height: 80%;
    margin-left: 24px;
    padding-right: 1px;
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
@media screen and (max-width: 844px) {
  .navigations__profiles__info,
  .navigations__profiles__tag {
    display: none;
  }
}
@media screen and (max-width: 767px) {
  .navigations__search__do {
    display: none;
  }
}
@media screen and (max-width: 414px) {
  .navigations__profiles__company,
  .navigations__profiles__name {
    display: none;
  }
}
</style>
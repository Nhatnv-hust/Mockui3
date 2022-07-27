<template>
  <div class="content">
    <div class="content__container">
      <div class="content__main">
        <div class="content__tree__search">
          <img src="../assets/configuration.svg" alt="" />
          <input type="text" />
        </div>
        <div class="content__tree__selcted">
          <div class="content__tree__search__name">{{ this.nameSelected }}</div>
          <div class="content__tree__search__select">
            <div class="content__selected">
              <img src="../assets/carvet.svg" alt="" />
              <p></p>
            </div>
            <div class="content__selected">
              <img src="../assets/carvet.svg" alt="" />
              <p></p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="content__content">
      <div class="content__content__title">
        {{ this.nameTitle1 }}
      </div>
      <div class="content__content__column">
        <div
          class="content__content__item"
          v-for="add in contents"
          :key="add.id"
        >
          <div class="content__content__item__header">
            <div class="content__content__label">
              <img :src="add.logo" alt="" />
              <p>{{ add.label }}</p>
            </div>
          </div>
          <div class="content__content__discip">{{ add.content }}</div>
        </div>
      </div>

      <!-- マスタ・ラベル管理 -->

      <div class="content__content__title">
        {{ this.nameTitle2 }}
      </div>
      <div class="content__content__column">
        <div
          class="content__content__item"
          v-for="add in contents2"
          :key="add.id"
        >
          <div class="content__content__item__header">
            <div class="content__content__label">
              <img :src="add.logo" alt="" />
              <p>{{ add.label }}</p>
            </div>
          </div>
          <div class="content__content__discip">{{ add.content }}</div>
        </div>
      </div>
    </div>
  </div>
  <!-- マスタ・ラベル管理 -->
</template>

<script>
export default {
  name: "Content-page",
  data() {
    return {
      nameSelected: "PEOPLE",
      nameTitle1: "PEOPLE設定一覧",
      nameTitle2: "マスタ・ラベル管理",
      contents: [
        {
          id: 1,
          logo: require("../assets/1.svg"),
          label: "管理者・会社情報設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 2,
          logo: require("../assets/2.svg"),
          label: "システム基本設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 3,
          logo: require("../assets/3.svg"),
          label: "管理者",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 4,
          logo: require("../assets/4.svg"),
          label: "アカウント",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 5,
          logo: require("../assets/5.svg"),
          label: "グループ設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 6,
          logo: require("../assets/6.svg"),
          label: "承認ルート設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 7,
          logo: require("../assets/7.svg"),
          label: "権限設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 8,
          logo: require("../assets/8.svg"),
          label: "ポジションコード設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 9,
          logo: require("../assets/9.svg"),
          label: "パスワード・二段階認証設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 10,
          logo: require("../assets/10.svg"),
          label: "外部サービス連携",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 11,
          logo: require("../assets/11.svg"),
          label: "データクレンジング",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 12,
          logo: require("../assets/12.svg"),
          label: "通知設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 13,
          logo: require("../assets/13.svg"),
          label: "インポート・エクスポート",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
      ],
      contents2: [
        {
          id: 14,
          logo: require("../assets/14.svg"),
          label: "発令マスタ",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 15,
          logo: require("../assets/15.svg"),
          label: "社員情報マスタ",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
        {
          id: 16,
          logo: require("../assets/16.svg"),
          label: "ラベル設定",
          content:
            "最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行までの説明最大３行まで",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
$font-stack: "Roboto", sans-serif;
$primary-color: #f5f5f5;
$background-color: #ffffff;

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.content {
  display: flex;
  // align-items: center;
}
.content__main {
  padding: 24px 20px 0px 12px;
}

.content__container {
  position: relative;
  top: 64px;
  width: 240px;

  background-color: #f8f8f8;

  .content__tree__search {
    height: 32px;
    display: flex;
    justify-content: start;
    align-items: center;
    margin-bottom: 24px;
    input {
      margin: 4px;
      outline: none;
      border: none;
      background-color: #f8f8f8;
    }
  }
  .content__tree__selcted {
    .content__tree__search__name {
      height: 40px;
      font-weight: 700;
      font-size: 16px;
      color: #007bc3;
      border-bottom: 1px solid #dcdcdc;

      .content__tree__search__select {
        display: flex;
        flex-direction: column;
      }
    }
  }
}
.content__content {
  top: 64px;
  position: relative;
  width: 100%;
  align-items: center;
  margin: 10px 100px;

  .content__content__title {
    margin-bottom: 24px;
    font-weight: 400;
    font-size: 20px;
    line-height: 30px;
    height: 24px;
    margin-top: 40px;
  }
}
.content__content__column {
  display: grid;
  grid-template-columns: auto auto auto;
  gap: 24px;
  font-family: "Roboto", sans-serif;
  .content__content__item {
    border: 1px solid #f5f5f5;
    border-radius: 8px;
  }
}
.content__content__item__header {
  background-color: #f8f8f8;
  border-bottom: 1px solid #f5f5f5;
}
.content__content__label {
  display: flex;
  justify-content: start;
  align-items: center;
  img {
    margin: 16px 8px 16px 16px;
    cursor: pointer;
  }
  p {
    margin: 20px 0px;
    font-weight: 400;
    font-size: 16px;
    word-break: break-all;
  }
}
.content__content__discip {
  padding: 16px;
  font-weight: 400;
  font-size: 12px;
}
</style>
<template>
  <div class="navList">
    <ul class="navLeft">
      <li class="navItem" v-for="(item, index) in items" :key="index">
        <router-link :to="'/' + item.ad">{{ item.name }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "navList",
  data() {
    return {
      items: [
        { name: "家里早起时间点", ad: "Home" },
        { name: "家里吃饭点点", ad: "Gream" },
        { name: "Echars", ad: "Echars" },
        { name: "图报表", ad: "Echearts01" },
        {name:"图表2", ad:"childEcher"}
      ]
    };
  }
};
</script>

<style scoped>
.navList {
  position: fixed;
  top: 50px;
  bottom: 0;
  left: 0;
  padding: 20px 40px;
  line-height: 40px;
  background-color: #293c55;
  overflow-y: auto;
  z-index: 15;
}
.navLeft {
  width: 168px;
  font-family: "Microsoft Yahei", sans-serif;
}
.navItem a {
  size: 14px;
  color: #b2b2b2;
}
.navItem a:hover {
  color: rgba(255, 255, 255, 0.8);
}
@media screen and (max-width: 964px) {
  #navList {
    position: relative;
    width: 100%;
    padding: 5px 20px;
    box-sizing: border-box;
    line-height: 20px;
  }
  .navLeft {
    width: 100%;
  }
  .navLeft .navItem {
    display: inline-block;
    margin: 5px 0;
    padding: 0 8px;
    border-right: solid 1px #b2b2b2;
  }
  .navItem:last-child {
    border-right: none;
  }
}
</style>

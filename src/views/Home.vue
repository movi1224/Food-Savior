<template>
  <div class="home">
    <el-container>
      <el-header style="margin-bottom: 50px">
        <el-row>
          <el-col :span="8">
            <img class="icon" :src="icon" />
          </el-col>
          <el-col :span="16" style="padding-right: 50px">
            <el-menu
              :default-active="activeIndex"
              class="header"
              mode="horizontal"
              @select="handleSelect"
              text-color="#000000"
              active-text-color="#FA4A0C"
            >
              <el-menu-item index="4">Contact</el-menu-item>
              <el-menu-item index="3">Our Mission</el-menu-item>
              <el-menu-item index="2">Product</el-menu-item>
              <el-menu-item index="1">Home</el-menu-item>
            </el-menu>
          </el-col>
        </el-row>
      </el-header>
      <el-main>
        <img class="page" :src="page1" />
        <!-- <div class="button_container">
          <el-button class="order_button">Order Now</el-button>
        </div> -->
      </el-main>
      <el-main>
        <img class="page" :src="page2" />
      </el-main>
      <el-main>
        <img class="page" :src="page3" /> </el-main
      ><el-main>
        <img class="page" :src="page4" /> </el-main
      ><el-main>
        <img class="page" :src="page5" /> </el-main
      ><el-main>
        <img class="page" :src="page6" />
      </el-main>
      <el-main>
        <img class="page" :src="footer" />
      </el-main>
    </el-container>
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from "@/components/HelloWorld.vue";
//import HeaderBar from '@/components/HeaderBar.vue';

export default {
  name: "Home",
  components: {
    //HelloWorld,
    //HeaderBar,
  },
  data() {
    return {
      activeIndex: "1",
      icon: require("/src/assets/logo_food_savior.jpg"),
      page1: require("/src/assets/page1.jpg"),
      page2: require("/src/assets/page2.jpg"),
      page3: require("/src/assets/page3.jpg"),
      page4: require("/src/assets/page4.jpg"),
      page5: require("/src/assets/page5.jpg"),
      page6: require("/src/assets/page6.jpg"),
      footer: require("/src/assets/footer.jpg"),
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style>
.header {
  font-weight: bold;
  float: right;
}
.icon {
  padding: 10px 0;
  padding-left: 80px;
  height: 100px;
  float: left;
}
.page {
  max-width: 100%;
  max-height: 100%;
  display: block;
  margin: auto;
}

.el-card__body,
.el-main {
  padding: 0px 20px 10px;
}
/* .button_container {
  width: 100%;
  height: 56px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 55%;
} */
/* .order_button {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 16px 0px;

  position: static;
  left: 0%;
  right: 0%;
  top: 0%;
  bottom: 0%;

  background: #fa4a0c;
  box-shadow: 0px 10px 30px rgba(183, 50, 39, 0.2);
  border-radius: 30px;

  /* Inside auto layout */

/* flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
} */
.el-menu-item {
  padding: 0 50px !important;
}

.el-menu > .el-menu-item.is-active {
  border: transparent !important;
}

.el-menu.el-menu--horizontal {
  border-bottom: none;
}

.el-menu--horizontal > .el-menu-item {
  float: right;
  height: 100px;
  line-height: 100px;
  margin: 0;
  border-bottom: 2px solid transparent;
  color: #909399;
}
</style>

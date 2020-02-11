<template>
  <article>
    <button  v-hammer:tap="onTap"></button>
    <!-- <user-item></user-item> -->
    <so-list style="margin-top: .8rem" v-for="(array,index) in list" :key="index" :listData="array"></so-list>
  </article>
</template>
<script>
// import SoList from "@/components/so-list.vue";
export default {
  name: "ME",
  components: {
    // SoList
  },
  data() {
    return {
      list: [
        [
          {
            name: "支付1",
            icon: require("../assets/icon/me/so-icon-pay.png")
          }
        ],
        [
          {
            name: "收藏",
            icon: require("../assets/icon/me/so-icon-collection.png")
          },
          {
            name: "相册",
            icon: require("../assets/icon/me/so-icon-img.png")
          },
          {
            name: "卡包",
            icon: require("../assets/icon/me/so-icon-cards.png")
          },
          {
            name: "表情",
            icon: require("../assets/icon/me/so-icon-smile.png")
          }
        ],
        [
          {
            name: "设置",
            icon: require("../assets/icon/me/so-icon-setting.png")
          }
        ]
      ]
    };
  },
  methods:{
    onTap:function(){
      console.log("hammer tap function");
    }
  }
};
</script>
<style lang="stylus" scoped>
article {
  box-sizing: border-box;
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
  width: 100%;
  height: 100%;
  background: #ededed;
}
</style>
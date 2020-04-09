<template>
  <div>
    <ul>
      <li v-for="item in list" :key="item.id">
        {{item.title}}
        <button @click="deleteItem(item.id)">删除</button>
      </li>
    </ul>
  </div>
</template>

<script>
// import event from "./event";

export default {
  //   props: ["list"],
  props: {
    list: {
      type: Array,
      default() {
        return [];
      }
    }
  },
  // props: {
  //     // prop 类型和默认值
  //     list: {
  //         type: Array,
  //         default() {
  //             return []
  //         }
  //     }
  // },
  data() {
    return {};
  },
  methods: {
    deleteItem(id) {
      this.$emit("delete", id);
    },
    handleEmit(title) {
      // eslint-disable-next-line
      console.log("handleEmit", title);
    }
  },
  //   created() {
  //     // eslint-disable-next-line
  //     console.log("list created");
  //   },
  //   mounted() {
  //     // eslint-disable-next-line
  //     console.log("list mounted");

  //     // 绑定自定义事件
  //     event.$on("onAddTitle",this.handleEmit);
  //   },
  //   beforeUpdate() {
  //     // eslint-disable-next-line
  //     console.log("list before update");
  //   },
  //   updated() {
  //     // eslint-disable-next-line
  //     console.log("list updated");
  //   },
  //   beforeDestroy() {
  //     // 及时销毁，否则可能造成内存泄露
  //     event.$off("onAddTitle",this.handleEmit)
  //   }
  beforeDestory() {
    // eslint-disable-next-line
    console.log("list beforeDestory");
  },
  destoryed() {
    // eslint-disable-next-line
    console.log("list destoryed");
  }
};
</script>
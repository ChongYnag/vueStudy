<template>
  <div>
    <input type="text" v-model="title" />
    <button @click="addItem()">add</button>
  </div>
</template>

<script>
//自定义事件
import event from "./event";

export default {
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addItem() {
      this.$emit("addItem", this.title);
      event.$emit("onAddTitle", this.title);
      this.title = "";
    }
    // addTitle() {
    //     // 调用父组件的事件
    //     this.$emit('add', this.title)

    //     // 调用自定义事件
    //     event.$emit('onAddTitle', this.title)

    //     this.title = ''
    // }
  },
//   beforeCreate() {
//     // eslint-disable-next-line
//     console.log("input", "beforeCreate");
//   },
//   created() {
//     // eslint-disable-next-line
//     console.log("input", "created");
//   }
};
</script>
<template>
  <div>
    <Input @addItem="addItem" />
    <List :list="list" @delete="deleteItem" />
  </div>
</template>

<script>
import Input from "./Input";
import List from "./List";

export default {
  components: {
    Input,
    List
  },
  data() {
    return {
      list: [
        {
          id: "id-1",
          title: "标题1"
        },
        {
          id: "id-2",
          title: "标题2"
        }
      ]
    };
  },
  methods: {
    addHandler(title) {
      this.list.push({
        id: `id-${Date.now()}`,
        title
      });
    },
    addItem(title) {
      this.list.push({
        id: `id-${Date.now()}`,
        title
      });
    },
    deleteItem(id) {
      this.list = this.list.filter(it => it.id !== id);
    }
  },
  beforeCreate() {
    // eslint-disable-next-line
    console.log("index beforeCreate");
  },
  created() {
    // eslint-disable-next-line
    console.log("index created");
  },
  beforeMount() {
    // eslint-disable-next-line
    console.log("index beforeMount");
  },
  mounted() {
    // eslint-disable-next-line
    console.log("index mounted");
  },
  beforeUpdate() {
    // eslint-disable-next-line
    console.log("index before update");
  },
  updated() {
    // eslint-disable-next-line
    console.log("index updated");
  },
  beforeDestory() {
    // eslint-disable-next-line
    console.log("index beforeDestory");
  },
  destoryed(){
      // eslint-disable-next-line
    console.log("index destoryed");
  }
};
</script>
<template>
  <div>
    <p>num {{num}}</p>
    <p>double1 {{double1}}</p>
    <input v-model="double2" />
    <a @click="add()">asdsad</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 20
    };
  },
  methods:{
      add(){
          this.num = this.num*2
      }
  },
  computed:{
      double1(){
          // eslint-disable-next-line
          console.log(1);
          return this.num*2
      },
      double2:{
          get(){
              return this.num*2
          },
          set(val){
              this.num = val/2
          }
      }

  },
    
};
</script>
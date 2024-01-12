<template>
    <h1>Comment</h1>
  <div class="the-comment">
    <textarea type="text" :value="modelValue" @input="handleInput" v-bind="$attrs" @click="handleclick"></textarea>
    <div class="text-right">
      <button>{{buttonText}}</button>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    modelValue: {
      type: String,
      default: "",
    },
    buttonText:{
        type: String,
        default: "OK",
    },
  },

//   inheritAttrs:false,

  mounted(){
    console.log(this.$attrs);
  },

  methods: {
    handleclick(e) {
      console.log("Click");
    },
    handleInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
    handleClick() {
      console.log("Click");
    },
  },
};
</script>
<style scoped>
.the-comment {
  width: 288px;
  border: 1px solid gray;
  padding: 22px;
  border-radius: 5px;
  background-color: azure;
  min-height: 111px;
}
textarea{
    padding: 7px 9px;
    margin-bottom: 11px;
    border-radius: 3px;
    width: 100%;
    border: 1px solid gray;
}
.text-right{
    text-align: right;
}
</style>

<template>
  <button @click="onClick()" class="btn" :style="{ background: color }">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
      default: "Button",
    },
    color: {
      type: String,
      required: false,
      default: "black",
    },
  },
  methods: {
    onClick() {
      this.$emit("btn-click");
    },
  },
};
</script>

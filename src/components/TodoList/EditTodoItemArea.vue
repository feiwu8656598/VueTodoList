<template>
  <input type="text" :placeholder="placeHolder">
</template>

<script>
export default {
  props: {
    placeHolder: String
  }
};
</script>
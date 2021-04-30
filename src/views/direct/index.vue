<template>
  <div class="direct">
    <CustomText tag="b" size="normal"> Direct Messages </CustomText>
  </div>
</template>

<script>
// @ is an alias to /src

import CustomText from "@/components/CustomText";

export default {
  name: "index",
  components: {
    CustomText,
  },
};
</script>

<style scoped></style>

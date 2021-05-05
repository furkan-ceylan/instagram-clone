<template>
  <div class="tag">
    <div class="tag-icon">
      <img src="../../img/tagged.jpg" alt="" />
    </div>
    <div class="tag-text">
      <div class="tag-text1">
      <CustomText class="thin" size="xlarge">
        Photos of you
      </CustomText>
      </div>
      <br />
      <div class="tag-text2">
      <CustomText size="normal">
        When people tag you in photos, they'll appear here.
      </CustomText>
      </div>
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";

export default {
  name: "tag",
  components: {
    CustomText,
  },
};
</script>

<style scoped>
.tag {
  display: grid;
  grid-template-rows: 100px 1fr;
  justify-content: center;
  align-items: center;
}

.tag-icon {
  width: 85px;
  height: 85px;
  justify-content: center;
  align-items: center;
  padding-left: 120px;
}

.tag-text {
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 50px;
}

.tag-text2 {
  max-width: 350px;
  max-height: 50px;
}

.thin {
  font-weight: 100;
  font-size: 25px;
}
</style>

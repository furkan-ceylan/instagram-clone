<template>
  <div class="save">
    <div class="save-icon">
      <img src="../../img/saved.jpg" alt="" />
    </div>
    <div class="save-text">
      <div class="save-text1">
      <CustomText class="thin" size="xlarge">
        Save
      </CustomText>
      </div>
      <br />
      <div class="save-text2">
      <CustomText size="normal">
        Save photos and videos that you want to see again. No 
        one is notified, and only you can see what you've saved.
      </CustomText>
      </div>
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";

export default {
  name: "save",
  components: {
    CustomText,
  },
};
</script>

<style scoped>
.save {
  display: grid;
  grid-template-rows: 100px 1fr;
  justify-content: center;
  align-items: center;
}

.save-icon {
  width: 85px;
  height: 85px;
  justify-content: center;
  align-items: center;
  padding-left: 135px;
}

.save-text {
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 50px;
}

.save-text2 {
  max-width: 350px;
  max-height: 50px;
}

.thin {
  font-weight: 100;
  font-size: 25px;
}
</style>

<template>
  <div class="igtv">
    <div class="igtv-icon">
      <img src="../../img/igrv.jpg" alt="" />
    </div>
    <div class="igtv-text">
      <CustomText class="thin" size="xlarge">
        Upload a Video
      </CustomText>
      <br />
      <CustomText size="normal">
        Videos must be between 1 and 60 minutes long.
      </CustomText>
    </div>
    <div class="igtv-upload">
      <button class="action-edit" type="button">
        <CustomText tag="b" size="normal">Upload</CustomText>
      </button>
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";

export default {
  name: "igtv",
  components: {
    CustomText,
  },
};
</script>

<style scoped>
.igtv {
  display: grid;
  grid-template-rows: 100px 1fr 1fr;
  justify-content: center;
  align-items: center;
}

.igtv-icon {
  width: 85px;
  height: 85px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  padding-left: 110px;
}

.igtv-text {
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.igtv-upload {
  width: 100px;
  height: 30px;
  padding-left: 105px;
  padding-top: 20px;
}

.action-edit {
  background-color: dodgerblue;
  padding: 0.5rem;
  border-radius: 3px;
  color: white;
  width: 100px;
  height: 30px;
}

.thin {
  font-weight: 100;
  font-size: 25px;
}
</style>

<template>
  <div class="post">
    <div class="post-media">
      <img
        src="https://www.instagram.com/static/images/mediaUpsell.jpg/6efc710a1d5a.jpg"
        alt=""
      />
    </div>
    <div class="share">
      <CustomText tag="b" size="xllarge">
        Start capturing and sharing your moments.
      </CustomText>
      <CustomText size="xlarge">
        Get the app to share your first photo or video.
      </CustomText>
      <div class="download-media">
        <img
          src="https://www.instagram.com/static/images/appstore-install-badges/badge_ios_english-en.png/180ae7a0bcf7.png"
          alt=""
        />
        <img
          src="https://www.instagram.com/static/images/appstore-install-badges/badge_android_english-en.png/e9cd846dc748.png"
          alt=""
        />
      </div>
    </div>
  </div>
</template>

<script>
import CustomText from "@/components/CustomText";

export default {
  name: "post",
  components: {
    CustomText,
  },
};
</script>

<style scoped>
.post {
  background-color: white;
  display: flex;
  justify-content: space-between;
}
.post-media {
  width: 380px;
  height: 380px;
}

.share {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-right: 100px;
}

.download-media {
  width: 135px;
  height: 40px;
  display: flex;
  flex-direction: row;
  padding-right: 120px;
  padding-top: 25px;
  cursor:pointer;
}
</style>

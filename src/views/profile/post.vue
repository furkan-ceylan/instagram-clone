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
    <div class="share-photos-mob">
    <div class="save-icon">
      <img src="../../img/photos.png" alt="" />
    </div>
    <div class="save-text">
      <div class="save-text1">
      <CustomText class="thin" size="xlarge">
        Share Photos
      </CustomText>
      </div>
      <br />
      <div class="save-text2">
      <CustomText size="normal">
        When you share photos, they will appear on your profile.
      </CustomText>
      </div>
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
  background-color: rgb(250,250,250);
}
.post-media{
  display: none;
}

.share {
  display: none;
}

.download-media {
  display: none;
}

.share-photos-mob { 
  display: flex;
  flex-direction: column;
  margin-left:auto;
  margin-right:auto;
  align-items: center;
  justify-content: center;
}

.share-photos-mob .save-text {
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 50px;
}

.share-photos-mob .save-text2 {
  max-width: 300px;
  max-height: 50px;
  align-items: center;
  justify-content: center;
}

.thin {
  font-weight: 100;
  font-size: 25px;
}


@media screen and (min-width: 980px) {
.post {
  background-color: white;
  display: flex;
  justify-content: space-between;
}
.post-media {
  display: inherit;
  width: 380px;
  height: 380px;
}

.share {
  display: inherit;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-right: 100px;
}

.download-media {
  display: inherit;
  width: 135px;
  height: 40px;
  display: flex;
  flex-direction: row;
  padding-right: 120px;
  padding-top: 25px;
  cursor:pointer;
}

.share-photos-mob {
  display: none;
}
}
</style>

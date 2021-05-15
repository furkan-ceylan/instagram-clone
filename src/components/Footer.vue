<template>
  <div class="footer">
      <ul class="footer-item">
          <li>About</li>
          <li>Blog</li>
          <li>Jobs</li>
          <li>Help</li>
          <li>API</li>
          <li>Privacy</li>
          <li>Terms</li>
          <li>Top Accounts</li>
          <li>Hashtags</li>
          <li>Locations</li>
      </ul>
      <ul>
          <li style="color: darkgray">© 2021 Instagram from github.com/fcyln</li>
      </ul>
  </div>
</template>

<script>
export default {
    name: 'Footer'

}
</script>

<style>

.footer{
    display: none;
}


@media screen and (min-width: 980px) {
.footer {
    display: flex;
    flex-direction: column;
    text-decoration: none;
    align-items: center;
    padding: 40px;
}

.footer ul {
    list-style: none;
}

.footer-item {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    padding-bottom: 10px;
}

.footer-item li{
    padding-right: 10px;
    color: darkgray;
    font-weight: 500;
    font-size: 12px;
}
}

</style>

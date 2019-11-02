<template>
  <x-page>
    <div class="container">
      <div class="row header-page">
        <div class="col-lg-6">
          <h1 class="header-title">{{data.title}}</h1>
          <h6>{{data.description}}</h6>
          <div class="landing-icons-container">
            <a target="_blank" v-if="data.github" :href="data.github" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://cdn.iconscout.com/icon/free/png-256/github-153-675523.png"
              />
            </a>
            <a target="_blank" v-if="data.gitlab" :href="data.gitlab" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://static.concrete.com.br/uploads/2019/06/logo-300x277.png"
              />
            </a>
            <a target="_blank" v-if="data.medium" :href="data.medium" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://image.flaticon.com/icons/png/512/174/174858.png"
              />
            </a>
            <a target="_blank" v-if="data.facebook" :href="data.facebook" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://cdn.icon-icons.com/icons2/1099/PNG/512/1485482214-facebook_78681.png"
              />
            </a>
            <a target="_blank" v-if="data.twitter" :href="data.twitter" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://cdn.icon-icons.com/icons2/1183/PNG/512/1490133460-social-icons01_82210.png"
              />
            </a>
            <a target="_blank" v-if="data.instagram" :href="data.instagram" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/58/Instagram-Icon.png/600px-Instagram-Icon.png"
              />
            </a>
            <a target="_blank" v-if="data.linkedlin" :href="data.linkedlin" class="icon-link">
              <img
                class="img-fluid icon-page"
                src="https://fatimamartinez.es/wp-content/uploads/2019/02/Logo-Linkedin.png"
              />
            </a>
          </div>
        </div>
        <div class="col-lg-6">
          <div style="text-align:center">
            <Avatar :circle="data.image.circle" :src="data.image.url" />
          </div>
        </div>
      </div>
    </div>
  </x-page>
</template>
<script>
import Avatar from "@/components/Avatar.vue";
import Data from "@/configs/landing.json";
export default {
  name: "home",
  components: { Avatar },
  data() {
    return {
      data: Data
    };
  }
};
</script>
<style scoped>
</style>
<template>
  <div id="app">
    <div style="height: 800px;">
    </div>
    <img id="profile_img" alt="profile" src="./assets/profile.jpeg">
    <h1>mikazuki</h1>
    <ScrollFadeIn>
      <ContentCard>
        <template v-slot:date>
          <p>2022/01</p>
        </template>
        <template v-slot:title>
          <p>大学入学</p>
        </template>
        <template v-slot:content>
          <p>入学したお<br>休学したいお</p>
        </template>
      </ContentCard>
    </ScrollFadeIn>
    <ScrollFadeIn>
      <ContentCard>
      </ContentCard>
    </ScrollFadeIn>
    <ScrollFadeIn><ContentCard></ContentCard></ScrollFadeIn>
  </div>
</template>

<script>
import ScrollFadeIn from './components/ScrollFadeIn.vue'
import ContentCard from './components/ContentCard.vue'

export default {
  name: 'App',
  data() {
    return {
    
    }
  },
  components: {
    ScrollFadeIn,
    ContentCard
}
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}

#profile_img {
  width: 130px;
  height: 130px;
  border: 5px solid green;
  border-radius: 50%;
}

</style>

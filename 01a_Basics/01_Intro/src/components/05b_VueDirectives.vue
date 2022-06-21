<template>
  <!--
    Vue Directives: Basic Directives (v-text, v-once, v-html, v-bind, v-if, v-show)
    -->
  <div>
    <h1 v-if="false" v-text="text">Loading...</h1>
    <h2 v-else-if="false" v-html="html" />
    <a
      v-else
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
      v-text="link.title"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      // v-text
      text: 'Openair Frauenfeld',
      // v-html
      html: 'grösstes</br>Hip-Hop Festival<br/><b>der Schweiz</b>',
      // v-bind
      link: {
        url: 'https://www.openair-frauenfeld.ch/',
        target: '_blank',
        tabindex: '0',
        title: 'Hier zur Openair Frauenfeld Webseite',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
h2 {
  margin: 40px 0 0;
  font-weight: normal;
}
a {
  display: block;
  margin-top: 40px;
}
</style>

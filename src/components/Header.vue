<template>
<a class="skip-to-content" href="#content">Skip to content</a>

<header aria-label="header">
  <div class="top-bar">
    <div class="container">
      <div class="logo">
        <a :href="`${logoHref}`">
            <span>
                <img :src="`${logo}`" :alt="`${title}`"/>
                <span class="mastTitle">{{mastTitle}}</span>
            </span>
        </a>
      </div>
      <div class="navigation">
        <slot></slot>
      </div>
    </div>
  </div>
  <div class="masthead">
    <div class="container">
      <a :href="`${titleHref}`">
        <h1>{{title}}</h1>
      </a>
    </div>
  </div>
</header>

</template>

<script>
export default {
  name: 'AviaryHeader',
  props: {
    logo: String,
    logoHref: {
        type: String,
        default: '#'
    },
    mastTitle:{
        type: String,
        default: "Texas A&M University Libraries"
    },
    titleHref: {
        type: String,
        default: 'https://library.tamu.edu'
    },
    title: {
        type: String,
        default: 'Aviary'
    },
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
        

</style>

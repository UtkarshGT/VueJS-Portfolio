<template>
<div class="uk-margin-medium-bottom">
  <h3 class="uk-heading-line uk-text-center punchline"><span>Some Projects</span></h3>
  <div class="uk-alert-primary" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p class="uk-text-center">Click on title for more details</p>
  </div>
  <ul uk-accordion="multiple: true">
    <li v-for="(project, index) in projects" v-bind:key="index">
      <a class="uk-accordion-title uk-text-center" href="#">{{ project.title }}</a>
      <div class="uk-accordion-content uk-text-center">
        <div class="uk-flex uk-flex-wrap uk-flex-center">
          <span v-for="(tech, index) in project.techstack" v-bind:key='index' class="uk-label uk-margin-right">{{ tech }}</span>
        </div>
        <p v-if="project.description">{{ project.description }}</p>
        <a v-if="project.link" :href="project.link" target="_blank" class="uk-button uk-button-primary">View Certificate</a>
        <div v-if="project.image" uk-lightbox><a class="uk-button uk-button-primary" :href="require(`@/assets/certificates/${project.image}`)">View Certificate</a></div>
        <hr>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {

  data(){
    return {
      
    }
  },
  props: {
    projects: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="less">

.ut-badge {
  background-color: cornflowerblue;
  color: white;
  border-radius: 20px;
  padding: 0 5px;
}

</style>
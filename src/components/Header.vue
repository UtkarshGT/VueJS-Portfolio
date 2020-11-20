<template>
  <header class="uk-flex uk-flex-column uk-margin-large-top">
    <div class="avatar uk-align-center uk-margin-small-bottom">
      <img src="../assets/man.png" alt="">
    </div>
    <div class="uk-align-center uk-margin-remove-vertical">
      <h3 class="user-name">{{ fullName }}</h3>
    </div>
    <div class="uk-align-center uk-margin-remove-bottom">
      <h3 class="uk-text-lead punchline">{{ punchline }}</h3>
    </div>
    <ul class="uk-flex uk-flex-center uk-comment-meta uk-subnav uk-subnav-divider uk-margin-remove-top">
      <li v-for="(skill, index) in skills" v-bind:key="index">{{ skill }}</li>
    </ul>
    <ul class="uk-flex uk-flex-center uk-comment-meta uk-subnav uk-subnav-divider uk-margin-remove-top uk-margin-medium-bottom">
      <li v-for="(academic, index) in academics" v-bind:key="index">{{ academic }}</li>
    </ul>

    
  </header>
</template>

<script>
export default {  

  data(){
    return {
      
    }
  },

  props: {
    fullName: {
      type: String,
      required: true
    },
    punchline: {
      type: String,
      required: false
    },
    skills: {
      type: Array,
      required: false
    },
    academics: {
      type: Array,
      required: false
    }
  }
}
</script>

<style lang="less" scpoed>

@avatar: 200px;

 img {
   width: 90%;
   padding: @avatar / 20;
 }

 .avatar {
   width: @avatar;
   height: @avatar;
   background-color: lightgray;
   border-radius: 50%;
   text-align: center;
 }

 .user-name {
   padding: 0.1em 0.3em;
   border-radius: 5px;
   background-color: #dee2ff;
   margin-bottom: 0;
 }

.punchline {
  font-family: 'Courier New', Courier, monospace;
  text-align: center;
}

</style>
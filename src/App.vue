<template>
  <div>
    <P-Header :fullName="fullName" :punchline="punchline" :skills="skills" :academics="academics"></P-Header>
    <P-About :projects="projects"></P-About>
    <P-Footer></P-Footer>
  </div>
</template>

<script>
// npm modules
import UIkit from 'uikit';
import Icons from 'uikit/dist/js/uikit-icons';

UIkit.use(Icons)

// Components
import Header from './components/Header'
import About from './components/About'
import Footer from './components/Footer'

export default {
  name: 'App',

  components: {
    'P-Header': Header,
    'P-About': About,
    'P-Footer': Footer
  },

  data(){
    return {
      // For Header
      fullName: "Utkarsh Tale",
      punchline: "I'm a Linux user exploring new Tech",
      skills: ["Python", "Javascript", "Linux", "Git", "HTML", "CSS", "VueJS", "Django"],
      academics: ["3rd Year CSE Student", "PRPCOEM Amravati"],

      // For Content Area
      projects: [
        {
          title: "FreeCodeCamp Responsive Web Design",
          description: "Nov-2020: Learnt Applied Visual Design, Accessibility, CSS Flexbox and Grid",
          techstack: ["HTML", "CSS"],
          link: "https://www.freecodecamp.org/certification/fcc0300e508-101f-4f93-be98-80a3720b2de4/responsive-web-design"

        },
        {
          title: "This Portfolio App",
          description: "Nov-2020: Made to Learn VueJS and basic designing",
          techstack: ['Vue JS', 'HTML', 'UIkit CSS', 'npm'],
          // image name stored in certificates folder
          image: ""
        },
        {
          title: "Machine Learning using Pytorch",
          description: "July-2020: Built Neural Networks especially CNNs and submitted project",
          techstack: ['Python', 'Pytorch library'],
          image: "jovian.jpg"
        },
        {
          title: "30 Days of Kotlin",
          description: "Jun-2020: Learned Kotlin and submitted an Android app project",
          techstack: ['Kotin'],
          image: 'kotlin.jpg'
        },
        {
          title: "Machine Learning Workshop",
          description: "Jan-2020: Introduction to Machine Learning and Classical ML Algorithms",
          techstack: ['Python', 'Jupyter'],
          image: 'wac_workshop.jpg'
        },
        {
          title: "Programming, DS with Python",
          description: "Mar-2019: First time introduced to DS/Algorithms, used Python to solve academic numericals",
          techstack: ['Python'],
          image: 'nptel_jan2019.jpg'
        }
      ]
    }
  }
}
</script>

<style lang='less'>
@import '../node_modules/uikit/src/less/uikit.less';

html, body {
  height: 100%;
}

</style>
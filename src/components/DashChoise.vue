<template>
      <component :is="currentComponent" />
  </template>
  
  <script>
  import Dashboard from './Content/Home/DashboardApp.vue';
  import Courses from './Content/Courses/Courses.vue';
  import Emploi from './Content/Emploi.vue';
  import Absence from './Content/AbsenceJustification.vue';
  import Activity from './Content/Activity.vue';

  
  export default {
    props: {
      selectedComponent: {
        type: String,
        required: true
      }
    },
    components: {
      Dashboard,
      Courses,
      Emploi,
      Absence,
      Activity,
    },
    computed: {
      currentComponent() {
        switch (this.selectedComponent) {
          case 'Dashboard':
            return 'Dashboard';
          case 'Courses':
            return 'Courses';
          case 'Emploi':
            return 'Emploi';
          case 'Absence':
            return 'Absence';
          case 'Activity':
            return 'Activity';
          default:
            return 'Dashboard'; 
        }
      },
    },
  };
  </script>
  
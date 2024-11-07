<template>
    <div class="dashboard">
          <News />
          <CpOfTheWeek />
          <Teachers />
        </div>
  </template>
  
  <script>
  import News from './NewsApp.vue';
  import CpOfTheWeek from './CpOfTheWeekApp.vue';
  import Teachers from './TeachersApp.vue';
  
  export default {
    components: {
      News,
      CpOfTheWeek,
      Teachers,
    }
  };
  </script>

    <style>
        .dashboard {
        display: grid;
        grid-template-columns: 2fr 1fr;
        gap: 20px;
        }
    </style>
  
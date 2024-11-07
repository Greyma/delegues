<template>
    <a-card title="CP of the week">
      <div v-for="(item, index) in cpData" :key="index" class="cp-item">
        <span>{{ item.day }} - {{ item.time }}</span>
      </div>
    </a-card>
  </template>
  
  <script>
  export default {
    data() {
      return {
        cpData: [
          { day: "SUN TIP", time: "8:00 - 8:30" },
          { day: "MON RPC", time: "12:00 - 14:30" },
          { day: "THU ISI", time: "9:40 - 10:40" },
          { day: "WED PFA", time: "14:30 - 15:40" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .cp-item {
    padding: 8px 0;
    background-color: #e6f7ff;
    margin: 4px 0;
    border-radius: 4px;
  }
  </style>
  
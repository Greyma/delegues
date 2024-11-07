<template>
    <div class="footer">
      <p>&copy; {{ currentYear }} UMBB DevUP. All rights reserved.</p>
    </div>
  </template>
  
  <script>
  export default {
    name : "FooterApp",
    data() {
      return {
        currentYear: new Date().getFullYear(),
      };
    },
  };
  </script>
  
  <style scoped>
  .footer {
    background-color: #2b5797;
    color: #ffffff;
    text-align: center;
    padding: 15px 0;
    font-size: 14px;
    font-family: Arial, sans-serif;
  }
  </style>
  
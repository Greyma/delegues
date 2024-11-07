<template>
    <div class="activities">
      <h3>Activities</h3>
      <a-card class="activities-card">
        <a-button type="primary" block class="activity-button">
          <a-icon type="question-circle" />
          <span>Request</span>
        </a-button>
        <a-button type="primary" block class="activity-button">
          <a-icon type="check-circle" />
          <span>Vote</span>
        </a-button>
        <a-button type="primary" block class="activity-button">
          <a-icon type="file-text" />
          <span>Formulaire</span>
        </a-button>
      </a-card>
    </div>
  </template>
  
  <script>
  import { Button, Card, Icon } from 'ant-design-vue';
  
  export default {
    name :"ActivityApp",
    components: {
      'a-button': Button,
      'a-card': Card,
      'a-icon': Icon,
    },
  };
  </script>
  
  <style scoped>
  .activities {
    padding: 20px;
    font-family: Arial, sans-serif;
  }
  
  h3 {
    margin-bottom: 1em;
    font-size: 20px;
    color: #333;
  }
  
  .activities-card {
    background-color: #f5f7fa;
    border-radius: 8px;
    padding: 10px;
  }
  
  .activity-button {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    margin: 10px 0;
    background-color: #2b5797;
    border: none;
    color: #fff;
  }
  
  .activity-button .anticon {
    margin-right: 8px;
    font-size: 18px;
  }
  
  .activity-button span {
    font-size: 14px;
  }
  </style>
  
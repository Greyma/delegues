<template>
    <div class="folder">
      <a-icon type="folder" style="font-size: 60px;" />
      <p>{{ name }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: "FoldersApp",
    props: {
      name: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .folder {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 10px;
    cursor: pointer;
  }
  .folder p {
    margin-top: 5px;
    font-size: 14px;
    color: #333;
  }
  </style>
  
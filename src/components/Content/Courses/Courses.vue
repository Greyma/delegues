<template>
    <div>
      <h2>Support de cours</h2>
      <div class="headeree">
        <Tabs />
        <div class="view-buttons">
          <a-icon type="appstore" class="view-icon" />
          <a-icon type="bars" class="view-icon" />
        </div>
      </div>
      <div class="folders-container">
        <Folder v-for="folder in folders" :key="folder" :name="folder" />
        
        <div class="folder add-folder">
          <AddFolder />
        </div>
      </div>
    </div>
    
  </template>
  
  <script>
  import Tabs from "./Tabs.vue";
  import Folder from "./Folder.vue";
  import AddFolder from "./AddFolder.vue";
  
  export default {
    name: "CoursesApp",
    components: {
      Tabs,
      Folder,
      AddFolder,
    },
    data() {
      return {
        folders: ["THP", "BDDA", "RI", "PFA", "RPC", "133E87", "ANGLAIS", "GPQ"],
      };
    },
  };
  </script>
  
  <style scoped>
  .headeree {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .view-buttons {
    display: flex;
  }
  .view-icon {
    font-size: 24px;
    cursor: pointer;
    margin-left: 10px;
  }
  .folders-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }
  .add-folder {
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
  }
  </style>
  
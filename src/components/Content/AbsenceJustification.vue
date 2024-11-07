<template>
    <div class="absence-justification">
      <h2>Justifier mon absence</h2>
      <div class="search-bar">
        <a-input-search placeholder="recherche" style="width: 200px;" />
        <a-button type="primary" icon="plus" class="add-button">ajouter</a-button>
      </div>
      <a-card class="absence-table-card" bordered>
        <h3>Absences justifiées</h3>
        <a-table :columns="columns" :dataSource="data" rowKey="num" pagination="{false}" />
      </a-card>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        columns: [
          {
            title: "Num",
            dataIndex: "num",
            key: "num",
            width: "10%",
          },
          {
            title: "Date",
            dataIndex: "date",
            key: "date",
            width: "15%",
          },
          {
            title: "Modules",
            dataIndex: "modules",
            key: "modules",
            width: "20%",
          },
          {
            title: "Heure",
            dataIndex: "heure",
            key: "heure",
            width: "20%",
          },
          {
            title: "Profs",
            dataIndex: "profs",
            key: "profs",
            width: "20%",
          },
          {
            title: "Document",
            dataIndex: "document",
            key: "document",
            width: "15%",
            customRender: (text) => `<a>${text}</a>`,
          },
        ],
        data: [
          { num: 1, date: "12-11-2024", modules: "RI, ...", heure: "8:00-14:30", profs: "Nom, ...", document: "just..." },
          { num: 2, date: "12-11-2024", modules: "RI, ...", heure: "8:00-14:30", profs: "Nom, ...", document: "just..." },
          { num: 3, date: "12-11-2024", modules: "RI, ...", heure: "8:00-14:30", profs: "Nom, ...", document: "just..." },
          { num: 4, date: "12-11-2024", modules: "RI, ...", heure: "8:00-14:30", profs: "Nom, ...", document: "just..." },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .absence-justification {
    padding: 20px;
    font-family: Arial, sans-serif;
  }
  
  h2 {
    margin-bottom: 1em;
    font-size: 24px;
  }
  
  .search-bar {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .search-bar a-input-search {
    margin-right: 10px;
  }
  
  .add-button {
    background-color: #2b5797;
    border: none;
  }
  
  .absence-table-card {
    border-radius: 8px;
  }
  
  .absence-table-card h3 {
    margin-bottom: 20px;
  }
  </style>
  
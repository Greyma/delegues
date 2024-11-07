<template>
    <a-card title="About teachers">
      <a-table :data-source="teachers" :columns="columns" row-key="num" />
    </a-card>
  </template>
  
  <script>
  export default {
    data() {
      return {
        teachers: [
          { num: 1, name: "azouz wasila", email: "az@gmail.com", office: "block 5" },
          { num: 2, name: "hamadouche", email: "hamadouche@gmail.com", office: "block 5" },
          { num: 3, name: "Mesbah", email: "mesbah@gmail.com", office: "block 5" },
        ],
        columns: [
          { title: 'Num', dataIndex: 'num', key: 'num' },
          { title: 'Name', dataIndex: 'name', key: 'name' },
          { title: 'Email', dataIndex: 'email', key: 'email' },
          { title: 'Office', dataIndex: 'office', key: 'office' },
        ],
      };
    },
  };
  </script>
  
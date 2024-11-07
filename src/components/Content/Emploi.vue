<template>
    <div class="schedule-container">
      <h2>Emploi du temps</h2>
      <p>TI 01 / 1 . Sem</p>
      <table class="schedule-table">
        <thead>
          <tr>
            <th>Saturday</th>
            <th>Sunday</th>
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
            <th>Thursday</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(row, rowIndex) in schedule" :key="rowIndex">
            <td v-for="(cell, colIndex) in row" :key="colIndex" :class="{ 'filled': cell }">
              {{ cell }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    name :"EmploiApp",
    data() {
      return {
        schedule: [
          ["", "THP", "", "", "", ""],
          ["trait de analyse", "", "bases de don avance", "", "", ""],
          ["", "", "", "", "", ""],
          ["", "", "", "", "", ""],
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .schedule-container {
    text-align: center;
    font-family: Arial, sans-serif;
  }
  
  h2 {
    margin-bottom: 0.5em;
  }
  
  p {
    margin-top: 0;
    font-weight: bold;
  }
  
  .schedule-table {
    width: 100%;
    border-collapse: collapse;
    background-color: #f0f4f8;
  }
  
  .schedule-table th {
    background-color: #2b5797;
    color: white;
    padding: 10px;
    font-weight: normal;
  }
  
  .schedule-table td {
    border: 1px solid #dfe3e8;
    padding: 15px;
    text-align: center;
    min-width: 100px;
  }
  
  .schedule-table td.filled {
    background-color: #4a90e2;
    color: white;
    font-weight: bold;
  }
  </style>
  
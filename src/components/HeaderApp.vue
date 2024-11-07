<template>
    <div class="header">
      <span>Bienvenue nom</span>
      <span class="info">nom prénom | 213000300899</span>
      <div class="icons">
        <a-icon type="bell" />
        <a-icon type="user" />
        <a-icon type="setting" />
      </div>
    </div>
</template>
  
<style scoped>
  .header {
    display: flex;
    justify-content: space-between;
    padding: 1em;
  }
  .info {
    margin-right: 1em;
  }
  .icons > * {
    margin-left: 10px;
  }
</style>
  
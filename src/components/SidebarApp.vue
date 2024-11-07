<template>
    <a-menu mode="inline" theme="dark" style="width: 200px;">
      <div class="sidebar-header">The delegate</div>
      <a-menu-item @click="selectComponent('Dashboard')" key="1" icon="home">Accueil</a-menu-item>
      <a-menu-item @click="selectComponent('Courses')" key="2" icon="book">Cours</a-menu-item>
      <a-menu-item @click="selectComponent('Emploi')" key="3" icon="Emploi">EDT</a-menu-item>
      <a-menu-item @click="selectComponent('message')" key="4" icon="message">Messages</a-menu-item>
      <a-menu-item @click="selectComponent('Absence')" key="5" icon="Absence">Absence</a-menu-item>
      <a-menu-item @click="selectComponent('Activity')" key="6" icon="Activity">Activity</a-menu-item>
      <a-menu-item @click="selectComponent('setting')" key="7" icon="setting">Settings</a-menu-item>
      <a-menu-item @click="selectComponent('logout')" key="8" icon="logout">Log out</a-menu-item>
    </a-menu>
  </template>
  
  <script>
export default {
  methods: {
    selectComponent(component) {
      this.$emit('selectComponent', component);
    },
  },
};
</script>

  <style scoped>
  .sidebar-header {
    font-size: 1.5em;
    padding: 1em;
    color: #fff;
    text-align: center;
  }
  </style>
  
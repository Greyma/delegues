<template>
  <div id="app">
    <div class="layout">
      <Sidebar @selectComponent="updateSelectedComponent" />
      <div class="content">
        <Header />
        <Dashboard :selectedComponent="selectedComponent" />
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from './components/SidebarApp.vue';
import Header from './components/HeaderApp.vue';
import Dashboard from './components/DashChoise.vue';


export default {
  components: {
    Sidebar,
    Header,
    Dashboard,
  },
  data() {
    return {
      selectedComponent: 'news', // Composant par défaut
    };
  },
  methods: {
    updateSelectedComponent(component) {
      this.selectedComponent = component;
    },
  },
};
</script>


<style scoped>
.layout {
  display: flex;
}
.content {
  flex: 1;
  padding: 1em;
}
</style>
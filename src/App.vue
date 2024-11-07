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
  
  <Footer />
</template>

<script>
import Sidebar from './components/SidebarApp.vue';
import Header from './components/HeaderApp.vue';
import Dashboard from './components/DashChoise.vue';
import Footer from './components/Footer.vue';


export default {
  components: {
    Sidebar,
    Header,
    Dashboard,
    Footer,
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
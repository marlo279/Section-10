<template>
  <base-card>
    <base-button @click="selectTab('stored-resources')">
      Stored Resources
    </base-button>
    <base-button @click="selectTab('add-resource')"> Add Resource </base-button>
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResources from './components/learning-resources/StoredResources.vue';
import AddResource from './components/learning-resources/AddResource.vue';

export default {
  components: {
    StoredResources,
    AddResource,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
    };
  },
  methods: {
    selectTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>

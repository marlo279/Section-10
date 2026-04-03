<template>
  <ul>
    <learning-resource
      v-for="resource in storedResources"
      :key="resource.id"
      :title="resource.title"
      :documentation="resource.documentation"
      :link="resource.link"
    ></learning-resource>
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';

export default {
  components: {
    LearningResource,
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          documentation: 'The official Vue.js documentation.',
          link: 'https://vuejs.org',
        },
        {
          id: 'google',
          title: 'Google',
          documentation: 'Learn to Google...',
          link: 'https://google.com',
        },
      ],
    };
  },
};
</script>

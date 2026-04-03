<template>
  <ul>
    <li v-for="resource in storedResources" :key="resource.id">
      <h3>{{ resource.title }}</h3>
      <p>{{ resource.documentation }}</p>
      <a :href="resource.link" target="_blank">Visit Resource</a>
    </li>
  </ul>
</template>

<script>
export default {
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

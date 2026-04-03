<template>
  <li>
    <div>
      <header>
        <h3>{{ title }}</h3>
        <button>Delete</button>
      </header>
      <p>{{ documentation }}</p>
      <nav>
        <a :href="link" target="_blank" rel="noopener noreferrer">
          View Resource
        </a>
      </nav>
    </div>
  </li>
</template>

<script>
export default {
  props: ['title', 'documentation', 'link'],
};
</script>

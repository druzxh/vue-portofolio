<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ title }}</h1>
    <h3>
      I build things for the web.
    </h3>
    <p>Get ready for something amazing!</p>

  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.5rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.5rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

p {
  text-align: center;
}

@media (min-width: 1024px) {
  h1 {
    font-weight: 500;
    font-size: 4.5rem;
    position: relative;
    top: -10px;
  }

  h3 {
    font-size: 2.5rem;
  }

  .greetings h1,
  .greetings h3 {
    text-align: left;
  }

  p {
    text-align: left;
  }
}
</style>

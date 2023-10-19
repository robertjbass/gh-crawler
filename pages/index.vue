<script setup lang="ts">
const route = useRoute();
const placeholderData = await(
  await fetch("https://jsonplaceholder.typicode.com/todos")
).json();
const data = ref(placeholderData);
</script>

<template>
  <UContainer class="my-8">
    <UCard>
      <code>
        <pre>{{ data }}</pre>
      </code>
    </UCard>
  </UContainer>
</template>

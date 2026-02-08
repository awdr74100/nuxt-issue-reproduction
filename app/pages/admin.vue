<script setup lang="ts">
const { data } = useAsyncData(
  "users",
  () => {
    return $fetch("https://jsonplaceholder.typicode.com/users");
  },
  {
    immediate: true,
    lazy: true,
  },
);
</script>

<template>
  <div>{{ data }}</div>
</template>

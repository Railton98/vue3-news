<script>
export default {
  data() {
    return {
      list: [
        { id: 1, name: "Vue" },
        { id: 2, name: "Vuex" },
        { id: 3, name: "Vue-router" }
      ]
    };
  }
};
</script>

<template>
  <h1>Hello Vue 3!</h1>
  <Teleport to="#title">
    My Person Title
  </Teleport>
  <Teleport to="#modal">
    <ul>
      <li v-for="item in list" :key="item.id">{{ item.name }}</li>
    </ul>
  </Teleport>
  <!-- <Portal target="#modal">
    <ul>
      <li v-for="item in list" :key="item.id">{{ item.name }}</li>
    </ul>
  </Portal> -->
</template>
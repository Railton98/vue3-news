<script>
import useHttpGet from '@/use/httpGet'

export default {
  name: "App",
  setup() {
    const { data, loading, error } = useHttpGet('/api/users')

    return { data, loading, error }
  }
}
</script>


<template>
  <div>
    <p v-if="loading">Carregando...</p>
    <p v-if="error != null">{{ error }}</p>
    <ul v-if="data.users">
      <li v-for="user in data.users" :key="user.id">{{ user.name }} {{ user.mobile }}</li>
    </ul>
  </div>
</template>

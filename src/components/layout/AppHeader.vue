<template>
  <header class="app-header">
    <RouterLink class="app-logo" to="/dashboard" aria-label="Ir para o dashboard">
      Tarefas Web
    </RouterLink>

    <nav class="app-nav" aria-label="Menu principal">
      <RouterLink to="/dashboard">Dashboard</RouterLink>
      <RouterLink to="/tarefas/nova">Nova tarefa</RouterLink>
      <RouterLink to="/perfil">Perfil</RouterLink>
      <button type="button" class="link-button" @click="logout">Sair</button>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',

  methods: {
    logout() {
      this.$store.dispatch('auth/logout')
      this.$router.push({ name: 'login' })
    }
  }
}
</script>

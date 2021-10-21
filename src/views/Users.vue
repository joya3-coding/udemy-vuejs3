<template>
  <div class="users">
    <h1>Users</h1>
    <router-link to="/users/1">ユーザー１</router-link>
    <router-link to="/users/2">ユーザー２</router-link>
    <hr>
    <h1>User No. {{ id }}</h1>
  </div>
</template>

<script>
export default {
  props: ["id"],
  watch: {
    $route(to, from) {
      alert(this.id)
      alert(`$routeがid:${from.params.id}からid:${to.params.id}に変わった。`)
    }
  }
}
</script>


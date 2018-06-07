<template>
<div class="container">
  <h1 class="text-center">La page App, la page principal ?</h1>
      <alert></alert>
</div>

</template>

<script>
// J'importe mes pages vue
import alert from './Alert.vue'
export default {
  // Je précise les nom de mes components à regarder
  components: { alert }
}
</script>


<template>
  <div>
      <AdminHeader />
    <nuxt />
  </div>
</template>

<script>
import AdminHeader from '@/components/admin/AdminHeader'
export default {
    components: {
        AdminHeader
    }
};
</script>

<style>
html {
  font-family: "Gelasio", serif;
}

body {
  margin: 0;
}
</style>

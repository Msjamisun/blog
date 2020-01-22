<template>
  <div>
    <Header @sidenavToggle="displaySideNav = !displaySideNav" />
    <SideNav :show="displaySideNav" @close="displaySideNav = false" />
    <nuxt />
  </div>
</template>

<script>
import Header from "@/components/navigation/Header";
import SideNav from "@/components/navigation/SideNav";

export default {
  components: {
    Header,
    SideNav
  },
  data() {
    return {
      displaySideNav: false
    };
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

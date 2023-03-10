<template>
  <div class="flex">
    <div class="w-3/12 h-screen bg-gray-700 sticky top-0">
      <VueSidebar />
    </div>

    <div class="w-full">
      <VueDashboard />
    </div>
  </div>
</template>

<script>
import VueSidebar from "./components/VueSidebar.vue";
import VueDashboard from "./pages/VueDashboard.vue";

export default {
  name: "App",
  components: {
    VueSidebar,
    VueDashboard,
  },
};
</script>
<style>
body {
  background-color: #dcdcdc;
}
</style>

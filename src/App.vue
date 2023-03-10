<template>
  <!--  -->
  <div class="flex">
    <div
      class="absolute left-0 w-3/12 h-screen bg-gray-700 z-[1035] lg:sticky lg:top-0"
      :style="myStyle"
      id="sidenav-1"
      data-te-sidenav-init
      data-te-sidenav-hidden="false"
      :data-te-sidenav-mode="sidenavMod"
      data-te-sidenav-content="#content"
    >
      <VueSidebar />
    </div>

    <div class="w-full" id="content">
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
  computed: {
    myStyle() {
      return window.innerWidth <= 768
        ? {
            transform: "translateX(-100%)",
            top: "76px",
          }
        : "";
    },
    sidenavMod() {
      return window.innerWidth <= 768 ? "over" : "side";
    },
  },
};
</script>

<style>
body {
  background-color: #dcdcdc;
}
</style>

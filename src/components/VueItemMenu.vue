<template>
  <div class="text-xs text-gray-500 uppercase px-5 mt-5 mb-2">
    {{ props.data.name }}
  </div>
  <div class="text-base text-gray-300 px-6"></div>
  <div
    class="text-base text-gray-300 px-6"
    v-for="(item, i) in props.data.items"
    :key="i"
  >
    <!-- Link -->
    <a
      v-if="item.type == 'urlLink'"
      :href="item.path"
      class="flex justify-between items-center py-2"
    >
      <span class="flex items-center">
        <div v-html="item.icon"></div>
        {{ item.name }}
      </span>
    </a>

    <!-- Group -->
    <a
      v-else
      data-te-collapse-init
      data-te-ripple-init
      data-te-ripple-color="light"
      :href="`#collapseNav${item.id}`"
      role="button"
      aria-expanded="false"
      :aria-controls="`collapseNav${item.id}`"
      class="flex justify-between items-center py-2"
      :data-received="`menu-received-${item.id}`"
      @click="toggleMarker"
    >
      <span class="flex items-center">
        <div v-html="item.icon"></div>
        {{ item.name }}
      </span>
      <span :id="`menu-received-${item.id}`">
        <svg
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          class="w-4 h-4"
          viewBox="0 0 24 24"
        >
          <path d="M6 9l6 6 6-6"></path>
        </svg>
      </span>
    </a>
    <div v-if="item.type == 'groupLink'">
      <div
        v-for="(group, ii) in item.data"
        :key="ii"
        class="!visible hidden"
        :id="`collapseNav${item.id}`"
        data-te-collapse-item
      >
        <a
          class="block py-1 pl-5 text-xs text-gray-400 uppercase hover:text-gray-300"
          :href="group.path"
        >
          {{ group.name }}
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  data: {
    type: Object,
    required: true,
  },
});

const toggleMarker = (el) => {
  setTimeout(() => {
    const ariaExpanded = el.target.getAttribute("aria-expanded");
    const dataReceived = el.target.getAttribute("data-received");
    const elReceived = document.getElementById(dataReceived);
    elReceived.innerHTML =
      ariaExpanded == "true"
        ? `
        <svg 
          class="w-4 h-4" 
          viewBox="0 0 24 24" 
          stroke="currentColor" 
          stroke-width="2" 
          fill="none" 
          stroke-linecap="round" 
          stroke-linejoin="round"
        >
          <path d="M12 5l7 7-7 7"></path>
        </svg>
    `
        : `
      <svg
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        class="w-4 h-4"
        viewBox="0 0 24 24"
      >
        <path d="M6 9l6 6 6-6"></path>
      </svg>
    `;
  }, 200);
};
</script>

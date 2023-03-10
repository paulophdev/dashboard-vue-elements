<template>
  <div class="h-16 flex items-center justify-center">
    <a href="#">
      <img src="@/assets/logo.png" style="width: 100px" alt="" loading="lazy" />
    </a>
  </div>
  <div>
    <VueItemMenu v-for="(menuItem, i) in menuItems" :key="i" :data="menuItem" />

    <div style="margin-bottom: 100px"></div>
  </div>
</template>

<script setup>
import VueItemMenu from "./VueItemMenu.vue";

const menuItems = [
  {
    name: "MENU",
    items: [
      {
        id: "g4as4",
        type: "urlLink", // urlLink or groupLink
        name: "Dashboard",
        path: "/",
        icon: `
        <svg
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="3"
          class="text-gray-300 w-4 h-4 mr-2"
          viewBox="0 0 24 24"
        >
          <path d="M22 11.08V12a10 10 0 11-5.93-9.14"></path>
          <path d="M22 4L12 14.01l-3-3"></path>
        </svg>
      `,
        data: [],
      },
      {
        id: "h5g5f",
        type: "groupLink", // urlLink or groupLink
        name: "Grupo 01",
        path: "#",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path d="M22 12h-4l-3 9L9 3l-3 9H2"></path>
          </svg>
        `,
        data: [
          {
            name: "Opçao 01",
            path: "/opcao01",
          },
          {
            name: "Opçao 02",
            path: "/opcao02",
          },
          {
            name: "Opçao 03",
            path: "/opcao03",
          },
        ],
      },
    ],
  },
  {
    name: "CADASTROS",
    items: [
      {
        id: "1g32s",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 01",
        path: "/cadastro01",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"></path>
            <circle cx="12" cy="7" r="4"></circle>
          </svg>
        `,
        data: [],
      },
      {
        id: "s7dj3",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 02",
        path: "/cadastro02",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <circle cx="6" cy="6" r="3"></circle>
            <circle cx="6" cy="18" r="3"></circle>
            <path d="M20 4L8.12 15.88M14.47 14.48L20 20M8.12 8.12L12 12"></path>
          </svg>
        `,
        data: [],
      },
      {
        id: "a65sd",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 03",
        path: "/cadastro03",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path
              d="M4 15s1-1 4-1 5 2 8 2 4-1 4-1V3s-1 1-4 1-5-2-8-2-4 1-4 1zM4 22v-7"
            ></path>
          </svg>
        `,
        data: [],
      },
    ],
  },
  {
    name: "APP",
    items: [
      {
        id: "j8k76",
        type: "groupLink", // urlLink or groupLink
        name: "App 01",
        path: "#",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z"></path>
          </svg>
        `,
        data: [
          {
            name: "Opçao 01",
            path: "/opcao01",
          },
          {
            name: "Opçao 02",
            path: "/opcao02",
          },
          {
            name: "Opçao 03",
            path: "/opcao03",
          },
        ],
      },
      {
        id: "26sf3",
        type: "groupLink", // urlLink or groupLink
        name: "App 02",
        path: "#",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path>
          </svg>
        `,
        data: [
          {
            name: "Opçao 01",
            path: "/opcao01",
          },
          {
            name: "Opçao 02",
            path: "/opcao02",
          },
          {
            name: "Opçao 03",
            path: "/opcao03",
          },
        ],
      },
    ],
  },
  {
    name: "CADASTROS",
    items: [
      {
        id: "1g32s",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 01",
        path: "/cadastro01",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"></path>
            <circle cx="12" cy="7" r="4"></circle>
          </svg>
        `,
        data: [],
      },
      {
        id: "s7dj3",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 02",
        path: "/cadastro02",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <circle cx="6" cy="6" r="3"></circle>
            <circle cx="6" cy="18" r="3"></circle>
            <path d="M20 4L8.12 15.88M14.47 14.48L20 20M8.12 8.12L12 12"></path>
          </svg>
        `,
        data: [],
      },
      {
        id: "a65sd",
        type: "urlLink", // urlLink or groupLink
        name: "Cadastro 03",
        path: "/cadastro03",
        icon: `
          <svg
            fill="none"
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="text-gray-300 w-4 h-4 mr-2"
            viewBox="0 0 24 24"
          >
            <path
              d="M4 15s1-1 4-1 5 2 8 2 4-1 4-1V3s-1 1-4 1-5-2-8-2-4 1-4 1zM4 22v-7"
            ></path>
          </svg>
        `,
        data: [],
      },
    ],
  },
];
</script>

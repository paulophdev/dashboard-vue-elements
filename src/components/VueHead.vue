<template>
  <nav
    class="sticky top-0 z-[1000] flex-no-wrap relative flex w-full items-center justify-between bg-neutral-100 py-4 shadow-md shadow-black/5 dark:bg-neutral-600 dark:shadow-black/10 lg:flex-wrap lg:justify-start"
    data-te-navbar-ref
  >
    <div class="flex w-full flex-wrap items-center justify-between px-6">
      <button
        class="block border-0 bg-transparent py-2 px-2.5 text-neutral-500 hover:no-underline hover:shadow-none focus:no-underline focus:shadow-none focus:outline-none focus:ring-0 dark:text-neutral-200"
        type="button"
        data-te-sidenav-toggle-ref
        data-te-target="#sidenav-1"
        aria-controls="#sidenav-1"
        aria-haspopup="true"
      >
        <span class="[&>svg]:w-7">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="h-7 w-7"
          >
            <path
              fill-rule="evenodd"
              d="M3 6.75A.75.75 0 013.75 6h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 6.75zM3 12a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 12zm0 5.25a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75a.75.75 0 01-.75-.75z"
              clip-rule="evenodd"
            />
          </svg>
        </span>
      </button>

      <!-- Right elements -->
      <div class="relative flex items-center">
        <!-- Notications -->
        <div class="relative" data-te-dropdown-ref>
          <a
            class="hidden-arrow mr-4 flex items-center text-neutral-500 hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:text-neutral-200 dark:hover:text-neutral-300 dark:focus:text-neutral-300 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
            href="#"
            id="dropdownNotify"
            role="button"
            data-te-dropdown-toggle-ref
            aria-expanded="false"
          >
            <span class="[&>svg]:w-5">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="currentColor"
                class="h-5 w-5"
              >
                <path
                  fill-rule="evenodd"
                  d="M5.25 9a6.75 6.75 0 0113.5 0v.75c0 2.123.8 4.057 2.118 5.52a.75.75 0 01-.297 1.206c-1.544.57-3.16.99-4.831 1.243a3.75 3.75 0 11-7.48 0 24.585 24.585 0 01-4.831-1.244.75.75 0 01-.298-1.205A8.217 8.217 0 005.25 9.75V9zm4.502 8.9a2.25 2.25 0 104.496 0 25.057 25.057 0 01-4.496 0z"
                  clip-rule="evenodd"
                />
              </svg>
            </span>
            <span
              class="absolute -mt-2.5 ml-2 rounded-full bg-red-700 py-0 px-1.5 text-xs text-white"
              >{{ notifications.length }}</span
            >
          </a>
          <div
            className="absolute w-60 left-auto right-0 z-[1000] float-left m-0 mt-10 hidden list-none overflow-hidden rounded-lg shadow-md shadow-gray-500 bg-white bg-clip-padding text-left text-base [&[data-te-dropdown-show]]:block"
            aria-labelledby="dropdownNotify"
            data-te-dropdown-menu-ref
          >
            <div
              className="bg-transparent py-4 px-4 text-sm font-normal text-neutral-700  active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
            >
              Notificações
            </div>
            <hr />
            <div
              className="max-h-60 h-full overflow-auto"
              v-for="(notify, i) in notifications"
              :key="i"
            >
              <div className="mb-1">
                <div
                  className="bg-transparent py-2 px-4 text-sm font-normal text-neutral-700 active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200"
                >
                  <p className="mb-1">{{ notify.content }}</p>
                  <span>{{ notify.date }}</span>
                </div>
              </div>
            </div>
            <hr />
            <div>
              <a
                className="block w-full text-center whitespace-nowrap bg-transparent py-4 px-4 text-sm font-bold text-neutral-700 hover:bg-neutral-100 active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
                href="#"
                data-te-dropdown-item-ref
              >
                Ver toda Atividade
              </a>
            </div>
          </div>
        </div>

        <!-- Perfil -->
        <div class="relative" data-te-dropdown-ref>
          <a
            class="hidden-arrow flex items-center whitespace-nowrap transition duration-150 ease-in-out motion-reduce:transition-none"
            href="#"
            id="dropdownPerfil"
            role="button"
            data-te-dropdown-toggle-ref
            aria-expanded="false"
          >
            <img
              src="https://tecdn.b-cdn.net/img/new/avatars/2.jpg"
              class="rounded-full"
              style="height: 25px; width: 25px"
              alt=""
              loading="lazy"
            />
          </a>
          <div
            className="absolute w-48 left-auto right-0 z-[1000] float-left m-0 mt-10 hidden list-none overflow-hidden rounded-lg shadow-md shadow-gray-500 bg-white bg-clip-padding text-left text-base [&[data-te-dropdown-show]]:block"
            aria-labelledby="dropdownPerfil"
            data-te-dropdown-menu-ref
          >
            <div
              className="w-full bg-transparent py-4 px-4 text-sm font-normal text-neutral-700  active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
            >
              paulophdev@gmail.com
            </div>
            <hr />
            <div>
              <a
                className="block w-full bg-transparent py-4 px-4 text-sm font-normal text-neutral-700 hover:bg-neutral-100 active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
                href="/profile"
                data-te-dropdown-item-ref
              >
                <span className="flex items-center">
                  <svg
                    fill="none"
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                  >
                    <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"></path>
                    <circle cx="12" cy="7" r="4"></circle>
                  </svg>
                  &nbsp; Seu Perfil
                </span>
              </a>
            </div>
            <div>
              <a
                className="block w-full bg-transparent py-4 px-4 text-sm font-normal text-neutral-700 hover:bg-neutral-100 active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
                href="/settings"
                data-te-dropdown-item-ref
              >
                <span className="flex items-center">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="currentColor"
                    class="h-5 w-5"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M11.078 2.25c-.917 0-1.699.663-1.85 1.567L9.05 4.889c-.02.12-.115.26-.297.348a7.493 7.493 0 00-.986.57c-.166.115-.334.126-.45.083L6.3 5.508a1.875 1.875 0 00-2.282.819l-.922 1.597a1.875 1.875 0 00.432 2.385l.84.692c.095.078.17.229.154.43a7.598 7.598 0 000 1.139c.015.2-.059.352-.153.43l-.841.692a1.875 1.875 0 00-.432 2.385l.922 1.597a1.875 1.875 0 002.282.818l1.019-.382c.115-.043.283-.031.45.082.312.214.641.405.985.57.182.088.277.228.297.35l.178 1.071c.151.904.933 1.567 1.85 1.567h1.844c.916 0 1.699-.663 1.85-1.567l.178-1.072c.02-.12.114-.26.297-.349.344-.165.673-.356.985-.57.167-.114.335-.125.45-.082l1.02.382a1.875 1.875 0 002.28-.819l.923-1.597a1.875 1.875 0 00-.432-2.385l-.84-.692c-.095-.078-.17-.229-.154-.43a7.614 7.614 0 000-1.139c-.016-.2.059-.352.153-.43l.84-.692c.708-.582.891-1.59.433-2.385l-.922-1.597a1.875 1.875 0 00-2.282-.818l-1.02.382c-.114.043-.282.031-.449-.083a7.49 7.49 0 00-.985-.57c-.183-.087-.277-.227-.297-.348l-.179-1.072a1.875 1.875 0 00-1.85-1.567h-1.843zM12 15.75a3.75 3.75 0 100-7.5 3.75 3.75 0 000 7.5z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                  &nbsp; Configurações
                </span>
              </a>
            </div>
            <hr />
            <div>
              <a
                className="block w-full bg-transparent py-4 px-4 text-sm font-normal text-neutral-700 hover:bg-neutral-100 active:text-neutral-800 active:no-underline disabled:pointer-events-none disabled:bg-transparent disabled:text-neutral-400 dark:text-neutral-200 dark:hover:bg-white/30"
                href="/"
                data-te-dropdown-item-ref
              >
                <span className="flex items-center">
                  <svg
                    class="w-5 h-5"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  >
                    <path d="M5 12h14"></path>
                    <path d="M12 5l7 7-7 7"></path>
                  </svg>
                  &nbsp; Sair
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
      <!-- /. Right elements -->
    </div>
  </nav>
</template>

<script setup>
const notifications = [
  {
    content:
      "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id, temporibus.",
    date: "10-03-2023 08:00",
  },
  {
    content: "Lorem ipsum dolor sit amet, adipisicing elit. Id.",
    date: "09-03-2023 12:30",
  },
  {
    content:
      "Lorem ipsum dolor sit amet, adipisicing elit, consectetur adipisicing.",
    date: "01-02-2023 16:25",
  },
];
</script>

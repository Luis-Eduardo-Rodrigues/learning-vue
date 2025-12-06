<template>
  <header class="flex items-center justify-between px-12 py-8 shadow-lg">
    <div>
      <h2 class="text-2xl font-medium">E-commerce Vuejs</h2>
    </div>
    <div class="relative w-72">
      <input
        type="text"
        placeholder="Buscar por um produto"
        class="px-4 py-2 pr-10 rounded-md w-full bg-zinc-100"
      />
      <i class="pi pi-search absolute right-3 top-1/2 -translate-y-1/2 text-zinc-500"></i>
    </div>

    <div class="flex items-center gap-8">
      <button>
        <i class="cursor-pointer text-xl rounded-md bg-zinc-600 p-2 text-white pi pi-user"></i>
      </button>
      <button>
        <i
          class="cursor-pointer text-xl rounded-md bg-zinc-600 p-2 text-white pi pi-shopping-cart"
        ></i>
      </button>
    </div>
  </header>
</template>

<style lang="scss" scoped></style>

<script setup></script>

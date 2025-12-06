<template>
  <main class="h-screen flex items-center justify-center bg-zinc-50">
    <form class="flex flex-col gap-6 shadow-xl py-8 px-12 bg-white">
      <div>
        <h2 class="text-2xl font-medium text-center">Criar conta</h2>
      </div>
      <div class="flex flex-col gap-3">
        <label class="text-left">Email <span class="font-bold text-red-600">*</span></label>
        <input
          class="w-72 px-4 py-2 rounded-md bg-zinc-100 text-md"
          type="email"
          placeholder="seuemail@email.com"
        />
      </div>
      <div class="flex flex-col gap-3">
        <label class="text-left">Seu nome <span class="font-bold text-red-600">*</span></label>
        <input
          class="w-72 px-4 py-2 rounded-md bg-zinc-100 text-md"
          type="text"
          placeholder="Nome completo"
        />
      </div>
      <div class="flex flex-col gap-3">
        <label class="text-left">Senha <span class="font-bold text-red-600">*</span></label>
        <input
          class="w-72 px-4 py-2 rounded-md bg-zinc-100 text-md"
          type="password"
          placeholder="********"
        />
      </div>
      <div>
        <button class="btn btn-success w-72 cursor-pointer text-white font-bold">
          Criar conta
        </button>
      </div>
      <div>
        <p class="text-center">
          Já tem uma conta?
          <a href="login" class="text-success font-bold cursor-pointer hover:underline">Entrar</a>
        </p>
      </div>
    </form>
  </main>
</template>

<script setup></script>

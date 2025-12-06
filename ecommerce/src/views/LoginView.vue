<template>
  <main class="h-screen flex items-center justify-center bg-zinc-50">
    <form class="flex flex-col gap-6 shadow-xl py-8 px-12 bg-white">
      <div>
        <h2 class="text-2xl font-medium text-center">Login</h2>
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
        <label class="text-left">Senha <span class="font-bold text-red-600">*</span></label>
        <input
          class="w-72 px-4 py-2 rounded-md bg-zinc-100 text-md"
          type="password"
          placeholder="********"
        />
      </div>
      <div>
        <a href="forgot-pw" class="text-right font-bold hover:underline">Esqueceu a senha?</a>
      </div>
      <div>
        <button class="btn btn-success w-72 cursor-pointer text-white font-bold">Entrar</button>
      </div>
      <div>
        <p class="text-center">
          Não tem uma conta?
          <a href="create" class="text-success font-bold cursor-pointer hover:underline"
            >Criar conta</a
          >
        </p>
      </div>
    </form>
  </main>
</template>

<script setup></script>

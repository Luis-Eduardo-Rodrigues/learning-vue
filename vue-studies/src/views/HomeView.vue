<template>
  <div class="p-12">
    <h2 class="my-4 text-2xl font-bold">Produtos</h2>
    <div class="flex items-center gap-4 flex-wrap">
      <div
        v-for="(produto, index) in arrProdutos"
        :key="index"
        class="card bg-base-300 w-96 shadow-sm rounded-md"
      >
        <figure>
          <img
            src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
            alt="Shoes"
          />
        </figure>
        <div class="card-body">
          <h2 class="card-title">
            {{ produto.nome }}
          </h2>
          <p>
            {{ produto.price }}
          </p>
          <p class="text-amber-400">
            {{ `Quantidade: ${produto.qtd}` }}
          </p>
          <div>
            <div
              v-for="(cor, indexColor) in produto.cores"
              :key="indexColor"
              aria-label="status"
              class="rounded-full status"
              :class="cor"
            ></div>
          </div>
          <div class="card-actions justify-end">
            <button class="btn btn-success rounded-md">Comprar</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const arrProdutos = [
  {
    nome: 'Tenis Nike',
    qtd: 50,
    cores: ['status-primay', 'status-secondary'],
    price: 'R$ 100,00',
  },
  {
    nome: 'Tenis Puma',
    qtd: 46,
    cores: ['status-success', 'status-accent'],
    price: 'R$ 200,00',
  },
  {
    nome: 'Tenis Olympikus',
    qtd: 20,
    cores: ['status-warning', 'status-neutral'],
    price: 'R$ 500,00',
  },
  {
    nome: 'Tenis Asics',
    qtd: 5,
    cores: ['status-info', 'status-error'],
    price: 'R$ 1000,00',
  },
]
</script>

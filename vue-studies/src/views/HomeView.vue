<template>
  <div class="p-12">
    <div class="card bg-base-300 w-96 shadow-sm rounded-md">
      <figure>
        <img
          src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
          alt="Shoes"
        />
      </figure>
      <div class="card-body">
        <h2 class="card-title">{{ nomeProduto }}</h2>
        <p>
          {{ description }}
        </p>
        <p>
          {{ quantidade }}
        </p>
        <div class="card-actions justify-end">
          <button class="btn btn-success rounded-md" @click="mudarQuantidade">
            Mudar quantidade
          </button>
          <button class="btn btn-success rounded-md" @click="changeName">Mudar nome</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const quantidade = ref(0)
const nomeProduto = ref('Tênis Nike')
const description = 'Tênis bem maneiro da nike.'

function changeName() {
  nomeProduto.value = 'Promoção tenis nike'
}

function mudarQuantidade() {
  quantidade.value++
}
</script>

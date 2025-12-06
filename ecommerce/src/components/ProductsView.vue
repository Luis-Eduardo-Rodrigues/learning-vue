<template>
  <div class="p-12 flex flex-col gap-4">
    <div>
      <h2 class="text-2xl font-medium">Produtos:</h2>
    </div>
    <div class="products-container flex items-center justify-center gap-4 flex-wrap">
      <div
        v-for="product in products"
        :key="product.id_product"
        class="card bg-base-100 w-96 shadow-sm"
      >
        <figure>
          <img
            src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
            alt="Shoes"
          />
        </figure>
        <div class="card-body">
          <h2 class="card-title">{{ product.product_name }}</h2>
          <span class="badge badge-primary">{{ product.category }}</span>
          <p>
            {{ product.description }}
          </p>
          <p>R$ {{ product.product_price }}</p>
          <p>Quantidade: {{ product.product_qtd }}</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary">Comprar</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { supabase } from '@/lib/supabase'
import { ref, onMounted } from 'vue'

const products = ref([])

async function fetchProducts() {
  const { data, error } = await supabase.from('products').select('*')

  if (error) console.log('Erro ao buscar os produtos: ', error)

  products.value = data
}

onMounted(() => fetchProducts())
</script>

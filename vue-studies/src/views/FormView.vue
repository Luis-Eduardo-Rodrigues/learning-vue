<template>
  <div class="h-screen flex items-center justify-center flex-col gap-4">
    <div>
      <fieldset class="fieldset">
        <legend class="fieldset-legend text-lg">
          Nome: <span class="font-bold text-red-600">*</span>
        </legend>
        <input
          v-model="form.nome"
          type="text"
          class="input w-72 rounded-md"
          placeholder="Seu nome"
        />
      </fieldset>
    </div>
    <div>
      <fieldset class="fieldset">
        <legend class="fieldset-legend text-lg">
          E-mail: <span class="font-bold text-red-600">*</span>
        </legend>
        <input
          v-model="form.email"
          type="text"
          class="input w-72 rounded-md"
          placeholder="Seu e-mail"
        />
      </fieldset>
    </div>
    <div>
      <fieldset class="fieldset">
        <legend class="fieldset-legend text-lg">
          Senha: <span class="font-bold text-red-600">*</span>
        </legend>
        <input
          v-model="form.senha"
          type="text"
          class="input w-72 rounded-md"
          placeholder="********"
        />
      </fieldset>
    </div>
    <div>
      <legend class="fieldset-legend text-lg">Estado:</legend>
      <select v-model="form.estado" class="select rounded-md w-72">
        <option disabled selected>Estado</option>
        <option value="ce">CE</option>
        <option value="sp">SP</option>
        <option value="rj">RJ</option>
      </select>
    </div>
    <div>
      <fieldset class="fieldset w-72 bg-base-100 border-base-300 rounded-box border p-4">
        <label class="label">
          <input v-model="form.isDev" type="checkbox" value="true" class="checkbox" />
          Programador?
        </label>
      </fieldset>
    </div>
    <div>
      <fieldset v-if="mostrarLing" class="fieldset">
        <legend class="fieldset-legend text-lg">
          Linguagem preferida: <span class="font-bold text-red-600">*</span>
        </legend>
        <input
          v-model="form.senha"
          type="text"
          class="input w-72 rounded-md"
          placeholder="Java, PHP, JavaScript"
        />
      </fieldset>
    </div>
    <div>
      <button @click="cadastrar" class="btn btn-success rounded font-bold text-lg">
        Cadastrar
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue'

const form = ref({
  nome: '',
  email: '',
  senha: '',
  estado: '',
  isDev: false,
  linguagem: '',
})

const mostrarLing = ref(false)
watch(
  () => form.value.isDev,
  (isDev) => {
    console.log('È programador: ', isDev)
    mostrarLing.value = isDev
  },
)

function cadastrar() {
  alert(JSON.stringify(form.value))
}
</script>

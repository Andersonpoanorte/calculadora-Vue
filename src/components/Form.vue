<script setup>
const props = defineProps(['valorNumero1', 'valorNumero2', 'trocarFiltro']);
</script>

<template>
    <form>
      <div class="d-flex flex-column align-items-center mt-4 gap-3">
        <div>
          <input @keyup="props.valorNumero1" type="number" class="form-control">
          <input @keyup="props.valorNumero2" type="number" class="form-control mt-3">
        </div>
        <div class="col">
          <select @change="props.trocarFiltro" class="form-control text-center">
            <option value="adicao">Adição</option>
            <option value="multiplicacao">Multiplicação</option>
            <option value="subtracao">Subtração</option>
            <option value="divisao">Divisão</option>
          </select>
        </div>
      </div>
    </form>
</template>
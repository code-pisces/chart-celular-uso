<template>
  <main>
    <article class="gap-3">
      <h1 class="text-5xl text-white font-bolder">Uso do Celular</h1>
      <p class="text-md text-slate-200">Foram entrevistados 30 alunos do CEHM, no turno matutino, sendo usada amostragem estratificada, com 5 alunos de
        cada turma. A partir dessas informações, foi possível traçar o tempo de uso médio por dia da semana de cada turma.
      </p>
      <p>Pesquisa realizada no dia 21/03/2023, escala de tempo em hora.</p>
    </article>

    <Chart />
  </main>
</template>

<script lang="ts" setup>
import Chart from './components/Chart.vue'
</script>

<style scoped>
main {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  width: 100%;
  height: 100vh;
}

h1 {
  font-family: 'Roboto Slab', sans-serif;
  text-transform: uppercase;
}

p {
  font-family: 'Roboto Slab', serif;
}

article {
  display: flex;
  flex-direction: column;
  text-align: center;
  max-width: 500px;
}
</style>
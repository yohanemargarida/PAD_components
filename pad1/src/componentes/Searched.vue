<template>
  <div>
    <div class="right" v-if="listTattooersFiltered.length && searched">
      <ul v-for="item in listTattooersFiltered" :key="item.id">
        <li>{{item.name}}</li>
      </ul>
    </div>

    <div class="right" v-else-if="searched && !listTattooersFiltered.length">
      <h4>Nome não encontrado: {{inputName}}</h4>
    </div>
  </div>
</template>
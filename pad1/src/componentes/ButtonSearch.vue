<template>
  <button
    :disabled="!inputName"
    @click="search"
    id="send"
    class="button-search"
    type="button">buscar</button>
</template>
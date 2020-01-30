<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/detalhes">Detalhes</router-link>
    </div>
    <router-view/>
    <Searched/>
    <Input/>
    
    <ButtonReturn/>
    
    
  </div>
  
</template>

<script>
import Input from './componentes/Input'
import Searched from './componentes/Searched'
import ButtonSearch from './componentes/ButtonSearch'
import ButtonReturn from './componentes/ButtonReturn'

export default {
   components: { Input, ButtonSearch, Searched, ButtonReturn },
}
</script>

<style>
</style>

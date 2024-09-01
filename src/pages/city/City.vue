<template>
  <div>
    <city-header></city-header>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/Head'
import CityList from './components/list'

export default {
  name: 'City',
  components: {
    CityHeader,
    CityList
  }
}
</script>

<style>

</style>
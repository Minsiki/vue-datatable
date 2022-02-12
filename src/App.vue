<template>
  <Datatable
    :columns="datatableData.columns"
    :datasource="datatableData.datasource"
  ></Datatable>
</template>

<script>
import Datatable from './components/datatable/Datatable.vue'

export default {
  name: 'App',
  components: {
    Datatable
  },
  data: () => {
    return {
      datatableData: {
        columns: [
          { prop: 'no', name: 'No', width: 100 },
          { prop: 'name', name: 'Name', width: 100 },
          { prop: 'email', name: 'e-mail', width: 200 },
          { prop: 'address', name: 'Address', width: 250 },
          { prop: 'rank', name: 'Rank', width: 80 },
          { prop: 'company', name: 'Company', width: 150 }
        ],
        datasource: [
          { no: '1', address: '서울 독산동', name: 'Kim', email: 'Kim@naver.com', rank: 'Manager', company: 'Naimnetworks' },
          { no: '2', name: 'Lee', email: 'Lee@gmail.com', address: '충북 개신동', rank: 'Manager', company: 'LoL' },
          { no: '3', name: 'Park', email: 'park@sixshop.com', address: '서울 사가정', rank: 'Manager', company: '6Shop' },
          { no: '4', name: 'Choi', email: 'choi@coopang.com', address: '서울 상계동', rank: 'Manager', company: 'Coopang' },
          { no: '5', name: 'Cho', email: 'cho@naimnetworks.com', address: '인천 어디동', rank: 'Manager', company: 'Naimnetworks' }
        ]
      }
    }
  },
  computed: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

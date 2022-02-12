<template>
<div class="datatable">
    <HeaderRow
        :columns="columns"
    ></HeaderRow>
    <DatatableBody :datasource="datasource" :columns="columns"></DatatableBody>
</div>
</template>
<script>
import HeaderRow from './header/row/HeaderRow.vue'
import DatatableBody from './body/DatatableBody.vue'
export default {
  name: '',
  components: { HeaderRow, DatatableBody },
  props: {
    columns: {
      type: Array,
      default: () => {
        return []
      }
    },
    datasource: {
      type: Array,
      default: () => {
        return []
      }
    }
  },
  data () {
    return {
      header: [],
      body: [],
      footer: []
    }
  },
  beforeCreate () {},
  created () {},
  beforeMount () {},
  mounted () {},
  beforeUpdate () {},
  updated () {},
  beforeUnMount () {},
  unmounted () {},
  methods: {}
}
</script>

<style scoped>
.datatable {
    width: 100%;
}
</style>

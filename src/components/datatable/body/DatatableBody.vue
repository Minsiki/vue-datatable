<template>
<div class="datatable-body">
    <BodyRow v-for="row of datasource" :key="row.no" :columns="columns" :row="row"></BodyRow>
</div>
</template>
<script>
import BodyRow from './BodyRow.vue'
export default {
  name: '',
  components: { BodyRow },
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
    return {}
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
.datatable-body {
    border: 1px solid #f0f0f0;
}
</style>

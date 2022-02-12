<template>
<div class="datatable-header-row">
    <HeaderRowCell v-for="column of columns" :key="column.no" :column="column">{{column.name}}</HeaderRowCell>
</div>
</template>

<script>
import HeaderRowCell from './cell/HeaderRowCell.vue'
export default {
  name: '',
  components: { HeaderRowCell },
  props: {
    columns: {
      default: null,
      type: [Object]
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

<style>
.datatable-header-row {
    display: flex;
    border: 1px solid #f0f0f0;
    border-radius: 3px;
    height: 40px;
}
</style>

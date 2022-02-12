<template>
<div class="datatable-body-row">
    <BodyRowCell
      v-for="column of columns"
      :key="column.no"
      :cell="row[column.prop]"
      :column="column"
      @on-header-cell-click="onCellClick">
    </BodyRowCell>
</div>
</template>
<script>
import BodyRowCell from './BodyRowCell.vue'
export default {
  name: '',
  components: { BodyRowCell },
  props: {
    row: {
      type: Object,
      default: () => {
        return {}
      }
    },
    columns: {
      type: Array,
      default: () => {
        return []
      }
    }
  },
  data () {
    return {}
  },
  computed: {},
  beforeCreate () {},
  created () {},
  beforeMount () {},
  mounted () {},
  beforeUpdate () {},
  updated () {},
  beforeUnMount () {},
  unmounted () {},
  methods: {
    onCellClick ($event) {
      console.log($event)
      this.$emit('onHeaderCellClick', $event)
    }
  }
}
</script>

<style scoped>
.datatable-body-row {
  display: flex;
  border-bottom: 1px solid #f0f0f0;
}

.datatable-body-row :last-child{
  border-bottom: none;
}

.datatable-body-row:hover {
  background-color: #cccccc;
  cursor: pointer;
}
</style>

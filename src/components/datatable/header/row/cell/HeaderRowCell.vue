<template>
    <div class="datatable-header-cell" :style="{width: `${column.width ? column.width : 100}px`}" @click="onHeaderCellClick">
        {{column.name}}
    </div>
</template>
<script>
export default {
  name: '',
  components: {},
  props: {
    column: {
      type: Object,
      default: () => {
        return {}
      }

    }
  },
  data () {
    return {
      componentName: 'datatable-header-cell'
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
  methods: {
    onHeaderCellClick ($event) {
      this.$emit('onHeaderCellClick', this.column)
    }
  }
}
</script>
<style scoped>
.datatable-header-cell {
  border-right: 1px solid #f0f0f0;
  text-align: center;
  line-height: 40px;
}

.datatable-header-cell :last-child {
  border-right: none;
}

.datatable-header-cell:hover {
  background-color: #c3c3c3;
  cursor: pointer;
}
</style>

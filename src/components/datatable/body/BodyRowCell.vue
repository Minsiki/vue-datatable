<template>
<div class="body-row-cell" :style="{width: `${column.width ? column.width : 100}px`}">{{cell}}</div>
</template>
<script>
export default {
  name: '',
  components: {},
  props: {
    cell: {
      type: String,
      default: () => {
        return ''
      }
    },
    column: {
      type: Object,
      default: () => {
        return {}
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
.body-row-cell {
  border-right: 1px solid #f0f0f0;
  text-align: center;
  line-height: 40px;
}

.body-row-cell :last-child {
  border-right: none;
}
</style>

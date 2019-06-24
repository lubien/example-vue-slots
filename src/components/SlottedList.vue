<template>
  <ul>
    <li v-for="(item, i) in list" :key="i">
      <slot :item="item">
        Fallback
      </slot>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'SlottedList',
  props: {
    list: {
      type: Array
    }
  }
}
</script>

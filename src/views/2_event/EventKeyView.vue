<template>
  <div>
<!--    <input type="search" name="" id="" @keyup="checkEnter($event)" v-model="searchText">-->
    <input type="search" name="" id="" @keyup.enter="doSearch()" v-model="searchText">
    <button @click="doSearch">조회</button>
  </div>
</template>

<script>
// @keyup List
// .enter
// .tab
// .delete
// .esc
// .space
// .up
// .down
// .left
// .down
// .ctrl

export default {
  components: {},
  data () {
    return {
      searchText: ''
    }
  },
  setup () {
  },
  created () {
  },
  mounted () {
  },
  unmounted () {
  },
  methods: {
    doSearch () {
      console.log(this.searchText)
    },
    checkEnter (event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>

<style scoped>

</style>

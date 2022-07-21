<template>
  <div>
    <button @click="incleaseCounter">Add 1</button>
    <p>{{counter}}</p>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      counter: 0
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
    incleaseCounter () {
      this.counter += 1
    }
  }
}
</script>

<style scoped>

</style>

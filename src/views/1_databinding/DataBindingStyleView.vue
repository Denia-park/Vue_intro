<template>
  <div>
    <div>
      스타일 바인딩 : 글씨는 red , 폰트크기:30px
    </div>
    <div v-bind:style="style1">
      스타일 바인딩 : 글씨는 green , 폰트크기:30px
    </div>
    <button @click="style1.color='blue'">색상 바꾸기</button>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      style1: {
        color: 'green',
        // font-size가 안되기 때문에 fontSize를 쓴다. 바닐라 JS에서도 동일함
        fontSize: '30px'
      }

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
  methods: {}
}
</script>

<style scoped>

</style>

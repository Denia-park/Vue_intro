<template>
  <div>
    <!--양방향 데이터 바인딩-->
    <input type="text" v-model="userId">
    <button @click="myFunction">클릭</button>
    <button @click="changeMyData">변경</button>
    <br>
    <!--  할당되는 값들은 문자열로 처리됨  -->
    <input type="text" v-model="num1"> +
    <input type="text" v-model="num2"> =
    <span>{{num1 + num2}}</span>
    <br>
    <!--  .number를 붙여줬기 때문에 할당되는 값들은 숫자로 처리됨  -->
    <input type="text" v-model.number="num3"> +
    <input type="text" v-model.number="num4"> =
    <span>{{num3 + num4}}</span>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      userId: 'Hyunggi',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0

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
    myFunction () {
      console.log(this.userId)
    },
    changeMyData () {
      this.userId = 'assaads'
    }
  }
}
</script>

<style scoped>

</style>

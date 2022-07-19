<template>
  <div>
    <div>
      <input type="checkbox" id="html" value="HTML" v-model="favoriteLang">
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="checkbox" id="css" value="CSS" v-model="favoriteLang">
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="checkbox" id="js" value="JS" v-model="favoriteLang">
      <label for="js">JavaScript</label>
    </div>
    <!--위의 체크박스에서 체크할때마다 아래에 선택된 값이 뜸 왜냐? v-model로 묶었기 때문에-->
    <!--checkbox는 사용자가 변경할 수 있는게 checked 속성밖에 없기-->
    <!--때문에 checked 속성이 변경되면 value 값을 가지고 와서 처리한다.-->
    <div>
      선택한 지역 : {{favoriteLang}}
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      // checkbox는 여러개를 선택할 수 있기 때문에
      // 배열로 data를 정의하고 바인딩 해야한다. ★반드시 배열★
      // 'JS' 값이 들어가있으면 사이트가 열릴때 JavaScript가 체크된 상태로 열림
      favoriteLang: []

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

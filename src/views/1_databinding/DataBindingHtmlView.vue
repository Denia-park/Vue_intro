<template>
  <div>
    <!--String 으로 할당됨    -->
    <div>{{htmlString}}</div>
    <!-- HTML로 할당됨   -->
    <div v-html="htmlString"></div>
  </div>
</template>

<script>
export default {
  name: 'FileName',
  components: {},
  data () {
    return {
      htmlString: '<p style="color:red;">빨간색 문자</p>'
    }
  },
  setup () {},
  created () {},
  mounted () {},
  unmounted () {},
  methods: {}
}
</script>

<style scoped>

</style>

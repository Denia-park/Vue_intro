<template>
  <div>
    <!--    active 처럼 한단어로 된 거면 '' 없어도 인식함-->
    <!--    text-red 같은 2단어 이상 조합은 '' 필요함-->
    <!--    <div :class="{'text-red':true , 'active':true}">-->
    <!-- Key-Value 형식 , value 는 Boolean 값이 들어간다  -->
    <!-- 엄청 많이 사용되는 방식 , class는 사용하는 방법이 조금 다르다 -->
    <div :class="{'text-red':hasError , 'active':isActive}">
      클래스 바인딩
    </div>
    <div :class="class2">
      클래스 바인딩 2
    </div>

  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      // 여기서 설정한 값에따라 class css가 적용되고 안되고 함
      isActive: false,
      hasError: true,
      // 아래의 방식은 많이 사용되지 않는다, 위처럼 많이 사용함
      class2: ['active', 'hasError']
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
.active{
  background-color:greenyellow;
  font-weight:bold;
}

.text-red {
  color:red;
}
</style>

<template>
  <div>
    <!-- @change === v-on:change 와 동일하다-->
    <!-- changeCity($event) 라고 하면 event 가 전달됨 -->
    <select name="" id="" @change="changeCity" v-model="selectedCity">
      <option value="">==도시선택==</option>
      <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList">{{city.title}}</option>
    </select>

    <select name="" id="">
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList">{{dong.dongTitle}}</option>
    </select>

    <select name="" id="">
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList.filter(dong => dong.cityCode === selectedCity)">{{dong.dongTitle}}</option>
    </select>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      cityList: [
        {
          title: '서울',
          cityCode: '02'
        },
        {
          title: '부산',
          cityCode: '051'
        },
        {
          title: '제주',
          cityCode: '064'
        }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울 1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울 2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울 3동' },
        { cityCode: '02', dongCode: '4', dongTitle: '서울 4동' },
        { cityCode: '051', dongCode: '1', dongTitle: '부산 1동' },
        { cityCode: '051', dongCode: '2', dongTitle: '부산 2동' },
        { cityCode: '051', dongCode: '3', dongTitle: '부산 3동' },
        { cityCode: '064', dongCode: '1', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '2', dongTitle: '제주 2동' }
      ],
      selectedDongList: [],
      selectedCity: ''
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
    changeCity () {
      this.selectedDongList = this.dongList.filter(dong => dong.cityCode === this.selectedCity)
    }
  }
}
</script>

<style scoped>

</style>

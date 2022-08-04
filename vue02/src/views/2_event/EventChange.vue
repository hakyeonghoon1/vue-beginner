<template>
  <div>
    <select name="" id="" @change="changeCity" v-model="selectedCity">
      <option value="">==도시선택==</option>
      <option :value="city.code" :key="city.code" v-for="city in cityList">
        {{ city.title }}
      </option>
    </select>
    <select name="" id="">
      <option
        :value="dong.dCode"
        :key="dong.dCode"
        v-for="dong in selectedDongList"
      >
        {{ dong.title }}
      </option>
    </select>
    <select name="" id="">
      <option
        :value="dong.dCode"
        :key="dong.dCode"
        v-for="dong in dongList.filter(
          (dong) => dong.cCode === this.selectedCity
        )"
      >
        {{ dong.title }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedCity: '',
      cityList: [
        { code: '02', title: '서울' },
        { code: '051', title: '부산' },
        { code: '064', title: '제주' }
      ],
      dongList: [
        { cCode: '02', dCode: 'd01', title: '서울1동' },
        { cCode: '02', dCode: 'd02', title: '서울2동' },
        { cCode: '02', dCode: 'd03', title: '서울3동' },
        { cCode: '02', dCode: 'd04', title: '서울4동' },
        { cCode: '051', dCode: 'd01', title: '부산1동' },
        { cCode: '051', dCode: 'd02', title: '부산2동' },
        { cCode: '051', dCode: 'd03', title: '부산3동' },
        { cCode: '051', dCode: 'd04', title: '부산4동' },
        { cCode: '051', dCode: 'd05', title: '부산5동' }
      ],
      selectedDongList: []
    }
  },
  methods: {
    changeCity() {
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cCode === this.selectedCity
      )
    }
  }
}
</script>

<style></style>

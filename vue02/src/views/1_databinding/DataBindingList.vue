<template>
  <div>
    <div>
      <select name="" id="">
        <option :value="city.code" :key="city.code" v-for="city in cities">
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>번호</th>
            <th>이름</th>
            <th>가격</th>
            <th>수량</th>
            <th>합계</th>
          </tr>
        </thead>
        <tbody>
          <tr :key="i" v-for="(drink, i) in drinkList">
            <td>{{ drink.id }}</td>
            <td>{{ drink.name }}</td>
            <td>{{ drink.price }}</td>
            <td><input type="number" name="" id="" v-model="drink.qty" /></td>
            <td>{{ drink.price * drink.qty }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      drinkList: [
        {
          id: '1',
          name: '음료1',
          price: '3000',
          qty: '2'
        },
        {
          id: '2',
          name: '음료2',
          price: '3000',
          qty: '2'
        },
        {
          id: '3',
          name: '음료3',
          price: '3000',
          qty: '2'
        },
        {
          id: '4',
          name: '음료4',
          price: '3000',
          qty: '2'
        },
        {
          id: '5',
          name: '음료5',
          price: '3000',
          qty: '2'
        }
      ]
    }
  }
}
</script>

<style></style>

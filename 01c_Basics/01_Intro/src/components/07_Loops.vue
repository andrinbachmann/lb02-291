<template>
  <!--
   Using v-for to Loop Over an Array of Strings
  -->
  <div>
    <h1>Looping through arrays (07_Loops.vue)</h1>
    <!-- Backticks -->
    <div v-for="n in 5" :key="`${n}`">
      {{ n }}
    </div>
    <!-- Unordered list -->
    <ul>
      <li v-for="n in 5" :key="n">
        {{ n }}
      </li>
    </ul>
    <!-- Unordered list with an array -->
    <ul>
      <li v-for="(item, n) in interests" :key="n">
        {{ item }}
      </li>
    </ul>
    <!-- Ordered list with objects -->
    <h3>Songs:</h3>
    <ol>
      <li v-for="item in songs" :key="item">
        {{ item }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      interests: ['Hip-Hop', 'Rock', 'Jazz', 'Techno'],
      songs: [
          {
            title: 'Its Now or Never',
            artist: 'Elvis Presley',
            sales: '21000000'
          },{
            title: 'Uptown Funk',
            artist: 'Mark Ronson',
            sales: '20000000'
          },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
li {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 10px;
}

h1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

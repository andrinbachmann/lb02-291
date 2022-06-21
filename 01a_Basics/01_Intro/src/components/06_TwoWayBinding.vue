<template>
  <!--
   TwoWayBinding Using v-model
  -->
  <section>
    <div>
      <h2 :class="$style.title">{{ title }}</h2>
      <h3 :class="$style.subtitle">{{ subtitle }}</h3>
    </div>
    <div :class="$style.form">
      <label>
        Vorname
        <input type="text" v-model="name" />
      </label>
      <label>
        Favorite Artist
        <select name="artist" v-model="artist">
          <option value="Sido">Sido</option>
          <option value="RIN">RIN</option>
          <option value="Gashi">Gashi</option>
          <option value="Stress">Stress</option>
        </select>
      </label>
    </div>
    <div :class="$style.overview">
      <h3>Anmeldung</h3>
      <ul>
        <li>Vorname: {{ name }}</li>
        <li>Favorite Artist: {{ artist }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: 'Openair Frauenfeld Registrierung',
      subtitle: 'Registriere dich um dabei zu sein',
      name: '',
      artist: ''
    }
  },
}
</script>

<style lang="scss" module>
.title {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 60px;
  background: lightgray;
}

.subtitle {
  color: #4fc08d;
  font-style: italic;
  text-align: center;
}

.form {
  display: flex;
  justify-content: space-evenly;
  max-width: 800px;
  padding: 40px 20px;
  border-radius: 10px;
  margin: 0 auto;
  background: #ececec;
}

.overview {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  max-width: 800px;
  margin: 40px auto;
  padding: 40px 20px;
  border-radius: 10px;
  border: 1px solid #ececec;

  > li {
    list-style: none;

    + li {
      margin-top: 20px;
    }
  }
}
</style>

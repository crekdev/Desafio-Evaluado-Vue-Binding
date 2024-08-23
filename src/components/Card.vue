<script>
export default {
  name: "Card",
  data() {
    return {
      cardTitle: "",
      cardNumber: "",
      dateExp: "",
      owner: "",
      urlChip: "../public/chip.png",
      urlVisa: "../public/visa.png",

    };
  },
};
</script>

<template>

  <body>
    <div id="app">
      <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input type="text" v-model="cardTitle" />
        </div>

        <div>
          <label>Chip SRC: </label>
          <input type="text" v-model="urlChip" />
        </div>

        <div>
          <label>Número: </label>
          <input type="number" v-model="cardNumber" />
        </div>

        <div>
          <label>Fecha de expiración: </label>
          <input type="text" v-model="dateExp" />
        </div>

        <div>
          <label>Propietario: </label>
          <input type="text" v-model="owner" />
        </div>

        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input type="text" v-model="urlVisa" />
        </div>
      </form>

      <div class="carnet">
        <h3>{{ cardTitle }}</h3>
        <img width="40" :src="urlChip" alt="" />
        <div>
          <h2>{{cardNumber}}</h2>
          <span>Fecha Exp: <b>{{dateExp}}</b></span>
        </div>
        <footer>
          <span>{{owner}}</span>
          <img :src="urlVisa" width="60" />
        </footer>
      </div>
    </div>
  </body>

</template>

<style scoped>
form {
  padding: 18px;
  border-radius: 20px;
  border: ridge 1px;
  box-shadow: 1px 1px 1px 1px gray;
  font-weight: bold;
  display: flex;
  flex-direction: column;
  gap: 15px;
  justify-content: center;
}

form div {
  display: grid;
  grid-template-columns: 100px 200px;
  align-items: center;
  gap: 5px;
}

form div label {
  text-align: right;
}

.carnet {
  width: 400px;
  height: 230px;
  background: #1c1a1e;
  color: white;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 0px 0px 10px 2px black;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
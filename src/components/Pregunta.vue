<template>
  <div class="container">
    <h1>Juego Yes or Not</h1>
    <img
      src="https://yesno.wtf/assets/no/19-2062f4c91189b1f88a9e809c10a5b0f0.gif"
      alt="No hay imagen"
    />

    <div class="container2"></div>
    <div class="pregunta-container">
      <input
        v-model="pregunta"
        type="text"
        id=""
        placeholder="Hazme una Pregunta?"
      />
      <p>Recuerda terminar con un signo de pregunta (?)</p>
      <h2>{{ pregunta }}</h2>
      <h1>{{ respuesta }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pregunta: null,
      respuesta: null,
    };
  },
  whatch: {
    pregunta(value, OldValue) {
      console.log("valor actual " + value);
      console.log("valor anterior " + OldValue);
    },
  },
};
</script>

<style scoped>
.container2,
img {
  height: 100vh;
  width: 100vw;
  max-height: 100%;
  max-width: 100%;
  position: fixed;
  left: 0px;
  top: 0px;
}
.container2 {
  background-color: rgb(0, 0, 0, 0.7);
}
.pregunta-container {
  position: relative;
}
input {
  width: 250px;
  padding: 10px 15px;
  border-radius: 5px;
  border: none;
  margin-top: 70px;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
input:focus {
  outline: none;
}
p {
  color: white;
  font-size: 25;
}
h1,
h2 {
  color: rgb(132, 102, 240);
}
h2 {
  margin-top: 60px;
}
</style>
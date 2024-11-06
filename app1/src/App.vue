<script>
export default {
  data() {
    return {
      city: "",
      error: ""
    }
  },
  methods: {
    getWeather(){
      if(this.city.trim().length < 2) {
        this.error = "Введите более одного символа"
        return false
      }

    }
  }
};
</script>

<template>
  <div class="container">
    <h1>Погодное приложение</h1>
    <p>Узнать погоду в {{ city== "" ? "вашем городе" : city }}</p>
    <input type="text"  v-model="city" placeholder="Введите город">
    <button v-show="city !=''" @click="getWeather()">Узнать</button>
    <p v-if="error">{{ error }}</p>
  </div>
</template>

<style scoped>
.container {
  width: 900px;
  height: 500px;
  border-radius: 50px;
  padding: 20px;
  background: #1f0f24;
  text-align: center;
  color: white;
}

.container h1 {
  margin-top: 50px;
}

.container p {
  margin-top: 20px;
}

.container input {
  margin-top: 30px;
  background: transparent;
  border: 0;
  border-bottom: 2px solid #110813;
  color: #fcfcfc;
  font-size: 14px;
  padding: 5px 8px;
  outline: none;
}

.container input:focus {
  border-bottom-color: #6e2d7d ;
}

.container button {
  background: #e3bc4b;
  color: #fff;
  border-radius: 10px;
  border: 2px solid #b99935;
  padding: 10px 15px;
  margin-left: 20px;
  cursor: pointer;
  transition: transform 500ms ease;
}

.container button:hover {
  transform: scale(1.1) translateY(-5px)
}
</style>

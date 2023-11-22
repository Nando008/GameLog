<script setup>
import { ref } from 'vue';


let one = ref(true)
let two = ref(false)
let three = ref(false)

function screenOne() {
  two.value = true
  one.value = false
  three.value = false
}

function screenTwo(){
  one.value = true
  two.value = false
  three.value = false
}

function screenThree(){
  three.value = true
  one.value = false
  two.value = false
}


</script>

<template>
  <body>
    <div class="container">
      
      <div v-show="one">
        <div class="ContainText">
          <h1 class="text">HOLA AMIGUITO!!</h1>
          <h1 class="text">Antes de comenzar esta emocionante aventura debes iniciar sesión</h1>
        </div>
      
        <div class="inputs">
          <input type="text" required>
          <label>Nombre de usuario</label>  
        </div>

        <div class="inputs">
          <input type="password" required>
          <label>Contraseña</label>  
        </div>

        <div class="button" @click="screenOne">
          <button>INICIAR</button>
        </div>

        <div class="button">
          <button href="" @click="screenThree">REGISTRATE</button>
        </div>
      </div>

      <div class="containerTwo" v-show="two">
        <div class="control">
          <img src="./Img/control.jpeg" alt="" height="290px" width="500px">
        </div>
        
        <h1 class="textExplicacion">1. Sensor tactil que mueve la nave horizontalmente hacia la izquierda</h1>

        <h1 class="textExplicacion">2. Sensor tactil que mueve la nave horizontalmente hacia la derecha</h1>

        <h1 class="textExplicacion">3. Sensor tactil de disparos con largo alcanze para derribar naves de la primera fila</h1>

        <h1 class="textExplicacion">4. Sensor tactil de disparos con corto alcnaze para derribar naves de la segunda fila</h1>

        <div class="button">
          <button href="">INICIAR EL JUEGO</button>
        </div>
      </div>

      <div>
        <div class="containerThree" v-show="three">
          
          <div class="bloque">
            <h1 class="bloqueText">HOLA AMIGUITO!!</h1>
            <h1 class="bloqueText">INGRESA LOS SIGUIENTES DATOS</h1>
            
            <div class="inputsbloque">
              <input type="text" required>
              <label>Primer Nombre</label>  
            </div>

            <div class="inputsbloque">
              <input type="text" required>
              <label>Segundo Nombre</label>  
            </div>
            
            <div class="inputsbloque">
              <input type="text" required>
              <label>Primer Apellido</label>  
            </div>

            <div class="inputsbloque">
              <input type="text" required>
              <label>Segundo Apellido</label>  
            </div>

            <div class="inputsbloque">
              <input type="text" required>
              <label>Genero</label>   
            </div>

            <div class="inputsEdad">
              <label>Fecha de nacimientos</label>
              <div>
                <input type="number" required placeholder="Día">
              </div>

              <div>
                <input type="number" required placeholder="Mes">
              </div>

              <div>
                <input type="number" required placeholder="Año">
              </div>
            </div>
          </div>

          <div class="bloque">
            <div class="bloquein">
              <h1 class="bloqueText">Crea un nombre de usuario</h1>
              
              <div class="inputsbloque">
                <input type="text" required>
                <label>Nombre de usuario</label>   
              </div>

              <h1 class="bloqueText">Crea una contraseña</h1>
              <div class="inputsbloque">
                <input type="text" required>
                <label>contraseña</label>   
              </div>

              <div class="buttonRegistro" @click="screenOne" >
                <button href="">REGISTARSE</button>
              </div>

              <div class="buttonRegistro" @click="screenTwo" >
                <button href="">REGRESAR</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<style scoped>

 body{
  margin: -22px -8px -8px -8px;
  background-color: rgba(82, 26, 2, 0.788);
  height: 560px;
  display: flex;
  justify-content: center;
  padding-top: 55px;
  padding-bottom: 40px;
  
}

.container{
  background-image: url(./Img/bg.png);
  height: 550px;
  width: 850px;
  border-radius: 15px;
}

.ContainText{
  margin-top: 50px;
  margin-bottom: 60px;
}

div > .text{
  justify-content: center;
  display: flex;
  background-color: rgba(255, 255, 255, 0.515);
  width: auto;
  margin: 10px 40px 5px 40px;
  border-radius: 10px;
  padding: 5px 0px 5px 0px;
  color: rgba(0, 0, 0, 0.853);
  font-family: Concert One;
  font-size: 25px;
}

.inputs{
  display: flex;
  justify-content: center;
  position: relative;
  margin-top: 30px;
  margin-bottom: 50px;
}

.inputs input{
  width: 500px;
  height: 50px;
  border-radius: 6px;
  font-size: 18px;
  padding: 0 15px;
  border: 2px solid #000000;
  background: transparent;
  color: #000000;
  outline: none;
  font-family: Concert One;
}

.inputs label{
  position: absolute;
  transform: translateY(-50%);
  top: 0;
  left: 180px ;
  font-size: 14px;
  padding: 2px 8px 2px 8px;
  background-color: #ffffffda;
  border-radius: 4px;
  color: #000000;
  font-family: Concert One;
}

.button{
  display: flex;
  justify-content: center;
  font-size: 20px;
  border-radius: 10px;
  background-color: rgba(255, 255, 255, 0.515);
  margin: 14px 40% 5px 40%;
  padding: 5px 0px 5px 0px;
  color: #000000;
  font-family: Concert One;
}

button {
  text-decoration: none;
  font-family: Concert One;
  background-color: transparent;
  border: none;
  border-bottom: 2px solid;
  font-size: 20px;
}

.button:hover {
  background-color: rgb(112, 2, 2);
  transition: 1s;
  color: #fff;
}

button:hover {
  color: #fff;
  transition: 0.30s;
}

.container > .containerTwo > .control{
  height: auto;
  width: 850px;
  display: flex;
  justify-content: center;
  margin: 18px 0 20px 0;
}

.textExplicacion {
  display: flex;
  flex-direction: column;
  background-color: rgba(255, 255, 255, 0.515);
  margin: 8px 40px 0px 40px;
  border-radius: 10px;
  padding: 5px 0px 5px 10px;
  color: rgba(0, 0, 0, 0.853);
  font-family: Concert One;
  font-size: 20px;
}

.containerThree { 
  display: flex;
  justify-content: space-around;
  margin: 30px 10px 0px 10px;
}

.bloque {
  background-color: rgba(118, 64, 64, 0.716);
  width: 400px;
  height: 494px;
  border-radius: 10px;
}

.bloqueText {
  justify-content: center;
  display: flex;
  background-color: rgba(255, 255, 255, 0.515);
  border-radius: 10px;
  padding: 5px 0px 5px 0px;
  color: rgba(0, 0, 0, 0.853);
  font-family: Concert One;
  font-size: 20px;
  margin: 10px 5px 0px 5px;
}

.inputsbloque {
  display: flex;
  justify-content: center;
  position: relative;
  margin: 20px auto;
}
.inputsbloque input{
  width: 300px;
  height: 40px;
  border-radius: 14px;
  font-size: 18px;
  padding: 0 15px;
  border: 2px solid #000000;
  background-color: rgba(255, 255, 255, 0.515);;
  color: #000000;
  outline: none;
  font-family: Concert One;
}

.inputsbloque label{
  position: absolute;
  transform: translateY(-50%);
  top: 0;
  left: 25%px ;
  font-size: 14px;
  padding: 2px 8px 2px 8px;
  background-color: #ffffffda;
  border-radius: 4px;
  color: #000000;
  font-family: Concert One;
}

.inputsEdad {
  display: flex;
  justify-content: center;
  position: relative;
  margin: 20px auto;
}

.inputsEdad input{
  width: 50px;
  height: 30px;
  border-radius: 14px;
  font-size: 18px;
  padding: 0 15px;
  border: 2px solid #000000;
  background-color: rgba(255, 255, 255, 0.515);;
  color: #000000;
  outline: none;
  font-family: Concert One;
  margin: 15px 2px 0px 2px;
}

.inputsEdad label{
  position: absolute;
  transform: translateY(-40%);
  top: 0;
  left: 25%px ;
  font-size: 14px;
  padding: 2px 8px 2px 8px;
  background-color: #ffffffda;
  border-radius: 4px;
  color: #000000;
  font-family: Concert One;
}

.bloquein{
  width: auto;
  height: 494px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.buttonRegistro{
  display: flex;
  justify-content: center;
  font-size: 20px;
  border-radius: 10px;
  background-color: rgba(255, 255, 255, 0.515);
  margin: 10px auto 0px auto;
  padding: 5px 5px 5px 5px;
  color: #000000;
  font-family: Concert One;
}

.buttonRegistro:hover {
  background-color: rgb(112, 2, 2);
  transition: 1s;
  color: #fff;
}

</style>

<script setup>

</script>

<template>
  <body>
    <div class="container">
      
      <div class="ContainText">
        <h1 class="text">HOLA AMIGUITO!!</h1>
        <h1 class="text">Antes de comenzar esta emocionante aventura debes iniciar sesión</h1>
      </div>
      
      <div class="inputs">
        <input type="text" required>
        <label>Nombre y apellido</label>  
      </div>

      <div class="inputs">
        <input type="password" required>
        <label>Contraseña</label>  
      </div>

      <div class="button">
        <a href="">INICIAR</a>
      </div>

      <div class="button">
        <a href="">REGISTRATE</a>
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
  margin-top: 15px;
  font-size: 20px;
  border-radius: 10px;
  background-color: rgba(255, 255, 255, 0.515);
  margin: 10px 40% 5px 40%;
  padding: 5px 0px 5px 0px;
  color: #000000;
  font-family: Concert One;
}


</style>

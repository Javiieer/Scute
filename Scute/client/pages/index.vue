<template >
  <div>
   
    <template v-if="useronline==true">
      <div >
        <Navbar></Navbar>
      </div>
    </template>
  
    <template v-else>
      <div>
        <div id="Homepagenav">
          <div id="logo">
            <img src="logo.png">
            <h2>Scute</h2>
          </div>
        </div>
        <div id="banner">
          <h1 class="title is-4">¡Loggeate y gana dinero subiendo tus dibujos!</h1>
          <div id="formu">
            <form v-if="userregister==true" action="get">
              <input type="text" placeholder="Usuario">
              <input type="text" placeholder="Contraseña">
              <button  class="button is-success is-fullwidth"><a href="#">Login</a></button>
              <span >¿No tienes una cuenta?</span>
              <a href="#">Registrate aquí!</a>
              <a href="#">¡Solo estoy de visita!</a>
            </form>
          </div>
        </div>
      </div>
      <footer><div id="foot">
            </div></footer>
    </template>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Logo, Navbar
  },
  head: {    
    link: [
      { rel: 'stylesheet', href: 'https://use.fontawesome.com/releases/v5.9.0/css/all.css' }
    ]
  },
  data() {
    return {
      useronline: false,
      userregister:true
    }
  },
  
}

</script>

<style>
#Homepagenav{
  
  height: 50px;
  width: 100%;
  background-color: #23d160;
  padding: 3px;
}
#logo{
  position: relative;
  left: 39%;
}
#Homepagenav img{
  width:  45px;
  height: 45px;
}
#Homepagenav h2{
display:inline-block;
font-size: 33px !important;
color: white;
}
#banner{
  background-image: url('https://thumbnails-photos.amazon.com/v1/thumbnail/s1vfevkHTJ6_vt9baEkDag?viewBox=1357%2C603&amp');
  width: 100%;
  height: 580px;
}
#foot{
  width: 100%;
  height: 20px;
  background-color: #23d160;
}

#formu{
  position: relative;
  background-color: white;
  height: 250px;
  width: 350px;
  padding: 1em;
  border-radius: 7px;
  opacity: .70;
  left: 33%;
  top: 120px ;

}

#formu input{
  height: 40px;
  width: 300px;
  margin: 1em;
  opacity: 1;
}
h1{
  position: relative;
  left: 28%;
  top: 110px;
  color: white !important;
}


</style>

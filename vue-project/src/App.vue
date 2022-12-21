<template>
    <NavBar></NavBar>
     
      <p class="boton" id="boton">Estrenos:</p> {{modifyMyFilm()}}
      <div class="text-container"></div>
      <div class="first-container">
     <img id="harry" class="harry" src="./assets/harry.webp" hidden width="230" height="180">
     </div>

     <div class="second-container">
     <p v-if="showOtherFilm">What lies Beneath?</p>
     
    </div>
     <p class="estrenos">Tendencias:</p>
     
     <ul>
      <div class="postlist" >
      <template v-for="post in posts" :key="post.id">
        <li> {{post.id}}. Título: {{ post.title }}, género: {{ post.genre }} </li>
      </template>
    </div>
     </ul>
     
     <div class="bottones">
      <div class="boton1">
     <button @click=modifyMyButton()>Estrenos en verde</button>
    </div>
    <div class="botton2">
     <button @click=resetMyButton()>Estrenos original</button>
    </div>
    </div>
    <div class="botones2">
    <div class="boton3">
      <button @click=showImage()>Click para mostrar imagen</button>
    </div>

    <div class="boton4">
      <button @click=hiddeImage()>Click para esconder la imagen</button>
    </div>
  </div>
    <FooterComponent></FooterComponent>
  
</template>

<script>

import NavBar from "./components/NavBar.vue";
import FooterComponent from "./components/FooterComponent.vue";
import posts from "./components/Posts.vue"

export default {
  components:{
    NavBar,
    FooterComponent,
    posts,
    
  
  },
  data(){
    return {
      myFilm:"",
      showOtherFilm:true,
      posts:[
        {id:1,title:"Harry Potter y la cámara de los secretos",genre:"fantasía"},
        {id:2,title:"Titanic",genre:"romance"},
        {id:3,title:"Spiderman",genre:"aventura"}
      ],
    }
    
  },
  methods:{
    modifyMyFilm(){
      return this.myFilm="Harry Potter y la piedra filosofal";

    },
    modifyMyButton(){
      document.getElementById("boton").style.background="green";
    },
    resetMyButton(){
     document.getElementById("boton").style.background=" rgb(79, 147, 167)";
    },
    showImage(){
      document.getElementById("harry").hidden=false;

    }, hiddeImage(){
      document.getElementById("harry").hidden=true;
    }
    
  }
}

</script>

<style scoped>

.boton{
  background-color: rgb(79, 147, 167);
  height: 25px;
  padding-top: 2px;
  padding-left: 10px;
  width: 75px;
  border-radius: 20px;
  color: white;
}

.estrenos{
  background-color: rgb(79, 147, 167);
  height: 25px;
  padding-top: 2px;
  padding-left: 10px;
  width: 90px;
  border-radius: 20px;
  color: white;
}

.postlist{
  display: block;  

}

.postlist li{
  list-style: none;
}

.bottones{
display: flex;
justify-content: center;
margin-top: 40px;

}

.botones2{
display: flex;
justify-content: center;
padding-right: 0px;
margin-top: 20px;
}

.first-container{
  margin-left: 20px;
  margin-top:10px
}




</style>

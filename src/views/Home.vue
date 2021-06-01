<template>
  <div class="home" v-if="isHomeLoaded">      
    <div class="image-container">
      <img class="big-image" src="../assets/home-page-photo.jpg" alt="Home Page Image">  
      <div class="question-text">Need to build a website?</div> 
      <div class="answer-text">We are here to help</div>
      <router-link to="/packages" tag="button" class="image-button">Checkout our Packages</router-link>
    </div> 
    <div class="services">
      <h2 class="heading">Our Services</h2>
      <div class="services-grid">
        <div class="grid-item">
          <img class="grid-image" src="../assets/services-grid-1.svg">
          <label class="grid-label">Fast and secure Web development</label>
        </div>
        <div class="grid-item">
          <img class="grid-image" src="../assets/services-grid-2.svg">
          <label class="grid-label">Fast and secure Web development</label>
        </div>
        <div class="grid-item">
          <img class="grid-image" src="../assets/services-grid-2.svg">
          <label class="grid-label">Fast and secure Web development</label>
        </div>
        <div class="grid-item">
          <img class="grid-image" src="../assets/services-grid-2.svg">
          <label class="grid-label">Fast and secure Web development</label>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data(){
    return{
      isHomeLoaded:'false'
    }
  },
  components: {
    
  },
  mounted(){
        document.onreadystatechange = () => {
            if(document.readyState == "complete"){
                this.isLoaded = true;
            }
        }
        
    } 
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif:wght@400;700&display=swap');
.home{
  padding-top: 1rem;
  text-align: center;
}
.image-container{
  width:100%;
  padding-bottom: 1rem;
  overflow: hidden;
  position: relative;
  color: #fff;
  font-family: 'Noto Serif', serif;  
}
.big-image{
  width: 100%;
}
.question-text{
  position: absolute;
  top: 2.5vw;
  right: 3%;
  font-size: 3.7vw;  
  font-weight: bold;
}
.answer-text{  
  position:absolute;
  top: 7.5vw;
  right: 3%;
  font-size: 3.2vw;
}
.image-button{
  position:absolute;
  top: 13vw;
  right: 3%;
  padding: 0.6rem 2rem;
  border-radius: 1.5rem;
  font-size: 1.15vw;
  font-weight: bold;
}
.services-grid{
  display: grid;
  grid-template-columns: auto auto;  
  padding: 10px;
}
.grid-image{
  width:80%;
}
.heading {
  font-size: 3vw;
  font-weight: bold;
}
.grid-label{
  font-size: 1.8vw;
}

</style>
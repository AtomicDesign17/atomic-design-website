<template>
  <div id="app">
    <div class="page-loader" v-if="!isLoaded">
       <moon-loader :color="color"></moon-loader>
    </div>
    <div class="header">    
        <img class="logo" src="./assets/logo250x100.png">
        <b-nav tabs fill>
          <b-nav-item to="/" exact exact-active-class="active">Home</b-nav-item>
          <b-nav-item to="/about" exact exact-active-class="active">About</b-nav-item>
          <b-nav-item to="/packages" exact exact-active-class="active">Packages</b-nav-item>
          <b-nav-item to="/contract" exact exact-active-class="active">Contact Us</b-nav-item>
        </b-nav>
        <!-- <div id="nav">
            <router-link to="/">Home</router-link> 
            <router-link to="/about">About</router-link> 
            <router-link to="/packages">Packages</router-link> 
            <router-link to="/contact">Contact Us</router-link>
        </div> -->
    </div>
    <div class="body" v-if="isLoaded" >
      <router-view/>
    </div>
  </div>
</template>

<script>
import MoonLoader from 'vue-spinner/src/MoonLoader'

export default {
  data:() => {
        return {
            isLoaded: false,
            color:"#FF9933"
        }
    },   
  components:{
    MoonLoader,
    
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

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans&display=swap');
.logo{
  width: 28%;
  max-width: 45rem;
  height: auto; 
  padding-bottom: 1rem;
}
.header{
  text-align: center;
}
.page-loader{
  justify-content: center;
  display: flex;
  padding-top:20%;
}
#app {
  padding: 1rem 1rem;
  font-family: 'Noto Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
}

#nav {
  padding: 4.063rem 6.25rem 0rem 0rem;
  float: right;
  
  a { 
    text-decoration: none;   
    color: #2c3e50;
    padding-left: 7.5rem;
          

    &.router-link-exact-active {
      color: #FF9933;
    }
  }
}
</style>

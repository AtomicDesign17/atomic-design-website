<template>
  <div class="home" v-if="isHomeLoaded">
    <div class="big-points">
      <div class="big-question">Need to make a web/mobile application?</div>
      <div class="big-answer">We are here to help</div>
    </div>
    <div class="web-design-section">
      <img class="web-design-layout" src="../assets/web-layout.png">
    </div>
    <div class="mobile-design-section">
      <img class="mobile-design-layout" src="../assets/mobile-layout.png">
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
.home{
  padding-top: 1rem;
  text-align: center;
}
.big-points{
  background-color: #FF9933;
  color: #FFF;
}
.big-question{
  font-weight: bold;
  font-size: 40px;
}
.big-answer{
  font-size: 40px;
  padding-top: 1rem;
}
.web-design-section{
  margin-top: 1rem;
  padding:1rem 0rem 1rem 0rem;
  text-align: left;
  background-color: #B3B3B3 ;
}
.web-design-layout{
  width:30%;
  height:auto;
  padding-left: 1rem;
}
.mobile-design-section{
  margin-top: 1rem;
  padding:1rem 0rem 1rem 0rem;
  text-align: right;
  background-color: #B3B3B3 ;
}
.mobile-design-layout{
  width: 15%;
  padding-right: 1rem;
}
</style>
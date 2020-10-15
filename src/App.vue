<template>
  <div id="app">
    <nav-bar></nav-bar>
    <router-view/>
  </div>
</template>

<script>
  import NavBar from '@/components/Nav'
export default {
  components: {
    NavBar
  }
}
</script>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
 
  margin: 2px;

 
 
  a {
    
    font-size: 22px;
    color: #fff;
    transition: all 0.3s ease 0s;
    &.router-link-exact-active {
      color: #42b983;
    }
      
 
  
   
  }
 

}
 .login{
    margin: 0px 20px 0px 40px;
    background:#1d1bed;
    border-radius: 24px;
    padding: 0px 20px;
    transition: all 0.3s ease 0s;
    box-shadow: 1px 1px 1px 1px lightblue;
    
  }
  .login:hover{
    background:#1d1bb3;
    
    
  }
 .logo{
   
   
   
   letter-spacing: 5px;
   
 }
</style>

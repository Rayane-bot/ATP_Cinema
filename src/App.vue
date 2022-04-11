<template>
  <div id="nav">
    <nav class="navbar" role="navigation" aria-label="main navigation">


      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-start">

          <a class="navbar-item">
            <router-link to="/">Acceuil</router-link>
          </a>

          <a class="navbar-item">
            <router-link to="/recherche">Recherche</router-link>
          </a>

          <div class="navbar-item has-dropdown is-hoverable">



          </div>
        </div>


      </div>
    </nav>
  </div>
  <router-view/>

</template>

<script>
export default {
  name: 'App',
  methods : {
    getList(){
      this.axios.get(api).then((response) => {
        console.log(response.data)
      })
    }
  }
}
</script>

<style>

  #navbarBasicExample.navbar-menu {
  align-content: center;
  }


  html, body, p, ol, ul, li, dl, dt, dd, blockquote, figure, fieldset, legend, textarea, pre, iframe, hr, h1, h2, h3, h4, h5, h6{
    color: white;
  }

  #app{
    background-color: dimgrey;
    min-height: 969px;
  }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: dimgrey;
}


</style>

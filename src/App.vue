<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>


<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {

  }
};
</script>

<style >

#app, body, html {
  max-height: 100vh;
  /* max-height: 100vh; */
  /* overflow: hidden; */
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

* {
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
}
/* html, body { height: 100%; width: 100%; margin: 0; } */
/* div { height: 100%; width: 100%;  } */
</style>

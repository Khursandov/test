<template>
  <div id="container">
    <router-link to="/second" id="start">Начать</router-link>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: "home",
  components: {
  },
  beforeCreate: function() {
    document.body.className = "home";
  }
};
</script>

<style scoped >
#container {
  background: #333;
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
  

#start {
  display: block;
  background: #fff;
  border-radius: 1vw;
  color: #333;
  text-decoration: none;
  font-size: 2vw;
  text-transform: uppercase;
  cursor: pointer;
  padding: 1vw 1vw;
}

a {
  cursor: pointer;
}
  
</style>


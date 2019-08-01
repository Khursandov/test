<template>
  <div>
    <Header colored="white" />
    <div class="clear"></div>
    <div class="content">
      <div class="content__left">
        <Slider />
      </div>
      <div class="content__right">

        <div class="form">
          <form v-on:submit.prevent="add">
            <label for="" >Ссылка на картинку</label>
            <input type="text" v-model="input" />
          </form>
        </div>
        
        <div class="add">
           <img src="../assets/svg/plus.svg" alt="" >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import Slider from "@/components/Slider.vue";
import Header from "@/components/Header.vue";
export default {
  name: "home",
  components: {
    Slider,
    Header
  },
  data() {
    return {
      isShown: false,
      isShown2: false,
      isShown3: false,
      input: ''
    }

  },
  created() {
    setTimeout(() => {
      this.isShown = true
      // alert('qwe')
    },2000)
  },
  methods: {
    intro1() {
      // console.log('222')
      this.isShown = !this.isShown
      this.isShown2 = true
    }
  }
};
</script>

<style scoped>
.content {
  display: flex;
  min-height: vw(400);
}
.content__left {
  width: 80%;
}
.content__right {
  text-align: center;
  width: 20%;
  background: greenyellow;
  color: #fff;
  padding: 40px 0;
  position: relative;
}
.content__right form{
  width: 70%;
  margin: auto;
  height: 63%;
}
.content__right form input{
  margin: 20px 0;
  padding: 7.5px 0;
}
.intro {
    position: absolute;
    width: 200px;
    z-index: 333;
    color: white;
    /* background: black; */
    right: 20%;
    text-align: end;
    padding: 0 25px;
    margin-top: 90px;
    transition: all 2s;
  
}
.intro p {
      line-height: 200%;
    font-weight: bold;
}
.intro button {
      padding: 10px 30px;
    background: red;
    border: none;
    box-shadow: none;
    border: none;
    color: #fff;
    cursor: pointer;
}
.content__right form ::after {
    content: "";
    position: absolute;
    width: 94px;
    height: 1px;
    background: white;
    margin-left: -48px;
    left: 0;
    z-index: 99;
    margin-top: 71px;
}
.add::after {
    content: "";
    position: absolute;
    width: 90px;
    height: 1px;
    background: white;
    margin-top: -20px;
    z-index: 999;
    margin-left: -90px;
    left: 0;
}
.add {
  height: 180px;
  width: 70%;
  text-align: bottom;
  margin: 0 auto;
  background: red;
  padding: 20px;
  position: absolute;
  bottom: 40px;
  margin-left: 15%;
}
.add img{
  width: 100%;
  height: 100%;
}

.clear {
  clear: both;
}
</style>


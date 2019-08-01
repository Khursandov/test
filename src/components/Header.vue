<template>
  <div class="header">
    <div class="header__logo header__logo--left leftArrow" :class="colored">
      <a href="#">
         <img src="../assets/svg/pl-logo.svg" alt="">
      </a>
    </div>
    <div class="header__logo header__logo--right rightArrow" :class="colored">
      <a href="#">
        <img src="../assets/svg/yt-logo.svg" alt="">
      </a>
    </div>
    <div class="clear"></div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    colored: String
  }
};
</script>

<style scoped >
.header {
  /* height: vw(160,$grid-breakpoints.lg); */
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* padding: 0 vw(40,$grid-breakpoints.lg) */
  position: relative;
  top: 0;
  width: 95%;
}
.leftArrow {
  width: 10%;
}

.leftArrow a img{
  width: 100%;
}

.rightArrow {
  margin: auto 0;
  width: 20%;
}
  .clear {
    clear: both;
  }
</style>


<template>
  <div class="home-container">
    <div class="d-copy">
      <h1>Comece a construir Agora !</h1>
      <h2>Contrua a sua presença online com a gente</h2>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.home-container {
  height: 600px;
  background-image: url("@/assets/images/banner.jfif");
  background-size: 100%;
  background-repeat: no-repeat;
  object-fit: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  @media (min-width: 300px) and (max-width: 599px) {
    background-size: 100% 100%;
    height: 300px;
  }
  @media (min-width: 600px) and (max-width: 999px) {
    background-size: 100% 100%;
    height: 400px;
  }

  .d-copy {
    color: $background;
    animation: bounce 4s infinite;
    h1 {
      letter-spacing: 3px;
      font-size: 48px;
      margin-bottom: 16px;
      @media (min-width: 300px) and (max-width: 599px) {
        font-size: 16px;
      }
      @media (min-width: 600px) and (max-width: 998px) {
        font-size: 30px;
      }
    }
    h2 {
      text-align: center;
      font-weight: normal;
      @media (min-width: 300px) and (max-width: 599px) {
        font-size: 12px;
      }
      @media (min-width: 600px) and (max-width: 998px) {
        font-size: 16px;
      }
    }
  }

  /*  .rocket-deploy {
    width: 350px;
    height: 350px;
    background-image: url("@/assets/images/rocket.svg");
    position: absolute;
    background-repeat: no-repeat;
    left: 0;
    @media (min-width: 200px) and (max-width: 500px) {
      width: 150px;
      height: 140px;
      text-align: center;
      position: static;
    }
    @media (min-width: 501px) and (max-width: 998px) {
      width: 180px;
      height: 200px;
      position: static;
    }

    @media (min-width: 999px) and (max-width: 1023px) {
      background-size: contain;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 250px;
      height: 270px;
    }
    @media (min-width: 1024px) and (max-width: 1279px) {
      height: 300px;
    }

    @media (min-width: 1280px) and (max-width: 1365px) {
    }
    @media (min-width: 1366px) and (max-width: 1440px) {
    }
  } */
}
</style>
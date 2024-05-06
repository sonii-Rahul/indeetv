<template>
  <div class="container">
    <div class="wrapper">
      <div class="heading">
        <img src="@/assets/logos.svg" alt="Global Distribution Logo">
        <h1>Global Distribution</h1>
      </div>
    </div>

    <div class="mainform">
      <Form />
    </div>

    <div class="bottom">
      <div class="fixedcontainer"></div>

      <div class="platform">
        <div class="bottomwrapper">
          <p class="subtitle">OTHER WAYS TO WATCH</p>
          <div class="socials">
            <img src="@/assets/apple.svg" alt="Apple TV">
            <img src="@/assets/ios.svg" alt="iOS">
            <img src="@/assets/roku.svg" alt="Roku">
            <img src="@/assets/amazon.svg" alt="Amazon">
          </div>
          <p class="searchtext">Search for AppleTV+ FYC on your App Store</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Form from './components/form.vue'
</script>

<style scoped>
.container {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background: rgba(0, 0, 0, 0.80);
  border-radius: 4px;
  height: 90vh;
  max-height: 620px;
  width: 90%; 
  max-width: 400px; 
  backdrop-filter: blur(5.5px);
  box-shadow: 0 0 0 4px #151515;
  overflow: hidden;
  font-family: "Noto Sans", sans-serif;
}

.wrapper {
  justify-content: center;
  width: 100%;
  display: flex;
}

.heading {
  display: flex;
  color: white;
  width: 278px;
  height: 74px;
  justify-content: center;
  align-items: start;
  margin-top: 30px;
}

.heading img {
  height: 80%;
  width: 30%;
}

.heading h1 {
  padding-left: 13px;
  width: 132px;
  height: 33px;
  margin: 0;
  font-size: 17px;
}

.mainform {
  padding: 0 30px;
}

.bottom {
  width: 100%;
  height: 273px;
  display: flex;
  flex-direction: column;
}

.fixedcontainer {
  height: 20%;
  width: 100%;
  background-color: #2D3137;
}

.platform {
  background-color: #24272C;
  color: #D5D5D5;
}

.bottomwrapper {
  display: flex;
  flex-direction: column;
  align-content: space-evenly;
  justify-content: space-evenly;
}

.platform p {
  display: flex;
  justify-content: center;
  text-align: center;
}

.subtitle {
  font-size: 10px;
  font-weight: bold;
}

.searchtext {
  font-size: 12px;
}

.socials {
  display: flex;
  justify-content: space-around;
  padding: 0 40px;
}

.socials img {
  width: 61.92px;
  height: 28px;
}

@media (max-height: 700px) {
  .container {
    height: 620px;
    width: 350px;
  }
}

@media (max-width: 400px) {
  .container {
    width: 320px;
    height: 580px;
  }

  .heading {
    width: 250px;
    height: 75px;
    justify-content: center;
    align-items: start;
    margin-top: 15px;
  }

  .heading img {
    height: 60%;
    width: 24%;
  }

  .heading h1 {
    width: 85px;
    height: 33px;
    font-size: 14px;
  }

  .socials img {
  width: 50px;
  height: 22px;
}
.fixedcontainer {
  height: 14%;
  width: 100%;
  background-color: #2D3137;
}
}
</style>

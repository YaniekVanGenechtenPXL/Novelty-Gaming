<template>
  <div id="container">
    <div id="minibanner">
        <div id="messageBox">
            <p>Free deliveries on orders of €25,00 or more!</p>
        </div>
    </div>
    <div id="banner"></div>
  </div>
</template>

<style lang="scss" scoped>
div#container {
    margin-top: 95px;
  div#minibanner {
    width: 100vw;
    height: fit-content;
    padding: 1vh 0;
    background-image: url(../assets/zebra.png);
    background-position: center center;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    div#messageBox {
        width: fit-content;
        padding: 5px 10px;
        background-color: #202020;
        border: 2px solid #FFFFFF;
        box-shadow: 0px 3px 6px rgba($color: #000000, $alpha: 0.16);
        p {
            color: white;
            font-weight: 300;
        }
    }
  }
  div#banner {
    width: 100vw;
    height: 500px;
    background-image: url(../assets/BannerBg.png);
    background-position: center center;
    background-size: cover;
  }
}
</style>
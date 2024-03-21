<template>
  <div id="container">
    <div id="leftside">
      <img :src="item.img" :alt="item.title" />
    </div>
    <div id="rightside">
      <h3>{{ item.title }}</h3>
      <p>{{ item.desc }}</p>
      <button>{{ item.buttonTxt }}</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
div#container {
    width: 42%;
    height: 16vw;
    display: flex;
    background-color: #231F20;
    div#leftside {
        width: 45%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        img {
            height: 90%;
        }
    }
    div#rightside {
        width: 55%;
        padding: 20px 20px 20px 0;
        position: relative;
        h3, p {
            text-align: right;
            color: #FFf;
        }
        h3 {
            font-weight: 400;
            font-size: 1.5vw;
        }
        p {
            font-weight: 300;
            font-size: 1.2vw;
        }
        button {
          width: 8vw;
          height: 3vw;
          position: absolute;
          bottom: 50px;
          right: 50px;
          font-weight: 300;
          font-size: 1vw;
        }
    }
}
</style>
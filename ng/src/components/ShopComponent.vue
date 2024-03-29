<template>
  <div id="shopContainer">
    <header>
      <select name="sort" id="sort" v-model="sort">
        <option value="featured">Featured</option>
        <option value="priceAsc">Price Ascending</option>
        <option value="priceDesc">Price Descending</option>
        <option value="nameAsc">A-Z</option>
        <option value="nameDesc">Z-A</option>
      </select>
    </header>
    <div id="shop__mainContainer">
      <aside>
        <div id="aside__content">
          <div id="clearContainer" @click="clearFilters">
            <img src="../assets/icons/clear.png" alt="clear" />
            <p>Clear all</p>
          </div>
          <div id="filtersContainer">
            <div id="searchFilter">
              <label for="search">Search within results</label>
              <input type="text" id="search" autocomplete="off" />
            </div>
            <div>
              <label for="select1">Price</label>
              <select name="select1" id="select1" v-model="select1">
                <option value="choose">Choose price</option>
                <option value="option1">Option 1</option>
                <option value="option2">Option 2</option>
                <option value="option3">Option 3</option>
                <option value="option4">Option 4</option>
              </select>
            </div>
            <div>
              <label for="select2">Model</label>
              <select name="select2" id="select2" v-model="select2">
                <option value="choose">Choose model</option>
                <option value="option1">Option 1</option>
                <option value="option2">Option 2</option>
                <option value="option3">Option 3</option>
                <option value="option4">Option 4</option>
              </select>
            </div>
            <div>
              <label for="select3">Color</label>
              <select name="select3" id="select3" v-model="select3">
                <option value="choose">Choose color</option>
                <option value="option1">Option 1</option>
                <option value="option2">Option 2</option>
                <option value="option3">Option 3</option>
                <option value="option4">Option 4</option>
              </select>
            </div>
            <div>
              <label for="select4">Material type</label>
              <select name="select4" id="select4" v-model="select4">
                <option value="choose">Choose material type</option>
                <option value="option1">Option 1</option>
                <option value="option2">Option 2</option>
                <option value="option4">Option 4</option>
                <option value="option3">Option 3</option>
              </select>
            </div>
            <div>
              <label for="select5">Size</label>
              <select name="select5" id="select5" v-model="select5">
                <option value="choose">Choose size</option>
                <option value="option2">Option 2</option>
                <option value="option3">Option 3</option>
                <option value="option4">Option 4</option>
              </select>
            </div>
          </div>
        </div>
      </aside>
      <main>
        <ProductComponent v-for="product in products" :key="product.id" :product="product" />
      </main>
    </div>
  </div>
</template>

<script>
import ProductComponent from '../components/ProductComponent.vue'
import productsData from '../products.json'

export default {
  components: {
    ProductComponent
  },
  data() {
    return {
      products: productsData,

      sort: 'featured',
      select1: 'choose',
      select2: 'choose',
      select3: 'choose',
      select4: 'choose',
      select5: 'choose'
    }
  },
  methods: {
    clearFilters() {
      this.select2 = 'choose'
      this.select1 = 'choose'
      this.select3 = 'choose'
      this.select4 = 'choose'
      this.select5 = 'choose'
    }
  }
}
</script>

<style lang="scss" scoped>
div#shopContainer {
  width: 80vw;
  margin: 0 auto;
  header {
    width: 100%;
    padding: 10px 0;
    display: flex;
    justify-content: flex-end;
  }
  div#shop__mainContainer {
    width: 100%;
    display: flex;
    aside {
      width: 18%;
      background-color: var(--black);
      margin-right: 2%;
      padding: 10px;
      div#aside__content {
        position: sticky;
        top: 110px;
        div#clearContainer {
          width: fit-content;
          display: flex;
          align-items: center;
          gap: 10px;
          margin: 10px auto;
          cursor: pointer;
          img {
            height: 20px;
          }
          p {
            font-size: 1rem;
            color: var(--white);
          }
        }
        div#filtersContainer {
          background-color: var(--white);
          div {
            padding: 10px;
            select {
              width: 100%;
              border: 1px solid var(--black);
              background-color: var(--white);
            }
          }
          div#searchFilter {
            input {
              width: 100%;
              border: 1px solid var(--black);
              background-color: var(--white);
              padding: 0 5px;
            }
          }
        }
      }
    }
    main {
      width: 80%;
      display: flex;
      justify-content: flex-start;
      flex-wrap: wrap;
      gap: 30px;
    }
  }
}

@media (max-width: 1100px) {
  div#shopContainer {
    div#shop__mainContainer {
      aside {
        width: 23%;
      }
      main {
        width: 75%;
      }
    }
  }
}
</style>
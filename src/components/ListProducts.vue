<template>
  <div class="list-products">
    <h1>{{ title }}</h1>

    <ul>
      <li v-for="product in products">
        <h3>{{ product.name }} <small>#{{ product.id }}<small></h3>
        <p>
          {{ product.description }}
        </p>
        <p class="price">{{ product.price | currency "R$ " }}</p>
      </li>
    </ul>
  </div>
</template>

<script>

var listProducts = [
  {
    "id"      : 1,
    "name"      : "Calça Jeans Masculina",
    "description" : "Calça jeans rajada, sizes P M G GG",
    "price"     : 89.90,
    "amount_off"  : 24,
    "price_off"   : 39.99,
    "image"     : "calca-jeans.jpg",
    "stock"     : 100
  },
  {
    "id"      : 2,
    "name"      : "Camisa Polo Masculina",
    "description" : "sizes P M G GG",
    "price"     : 1.00,
    "amount_off"  : 24,
    "price_off"   : 0.89,
    "image"     : "camiseta-polo.jpg",
    "stock"     : 200
  },
  {
    "id"      : 3,
    "name"      : "Sapatenis",
    "description" : "Sapatenis estiloso",
    "price"     : 129.90,
    "amount_off"  : 24,
    "price_off"   : 89.99,
    "image"     : "sapatenis.jpg",
    "stock"     : 100
  },
  {
    "id"      : 4,
    "name"      : "Bermuda Masculina",
    "description" : "Bermuda jeans masculina, sizes P M G ",
    "price"     : 29.90,
    "amount_off"  : 24,
    "price_off"   : 9.99,
    "image"     : "bermuda.jpg",
    "stock"     : 100
  },
  {
    "id"      : 5,
    "name"      : "Calça Moletom",
    "description" : "sizes P M G GG",
    "price"     : 78.90,
    "amount_off"  : 24,
    "price_off"   : 60.00,
    "image"     : "calca-moletom.jpg",
    "stock"     : 100
  },
  {
    "id"      : 6,
    "name"      : "Jaqueta de couro",
    "description" : "sizes P M G GG",
    "price"     : 279.90,
    "amount_off"  : 24,
    "price_off"   : 10.99,
    "image"     : "jaqueta-couro.jpg",
    "stock"     : 100
  }
]
export default {
  data () {
    return {
      // Note: modifying `msg` below will not cause changes to occur with
      // hot-reload. As reloaded components preserve their initial state,
      // modifying these values will have no effect.
      title: 'Produtos',
      products : listProducts
    }
  }
}
</script>
<style>
  ul{
    margin: 0;
    padding: 0;
    list-style: none;
  }
  ul li{
    float: left;
    display: block;
    width: 250px;
    min-height: 180px;
    margin: 5px;
    padding: 10px;
    box-sizing: boder-box;
    border: 1px solid #E8E8E8;
    box-shadow: 1px 2px 5px #E5E5E5;
  }

  ul li h3{
    color: #09233C;
  }
  ul li h3 small{
    color: #555;
  }
  ul li p{
    font-size: 18px;
  }
  ul li .price{
    color: #4B8A20;
    font-size: 24px;
  }
</style>

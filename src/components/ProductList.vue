<template>
    <div class="product-list">
      <h2>Product List</h2>
      <ul>
        <li v-for="product in products" :key="product.id">
          <h3>{{ product.name }}</h3>
          <p>{{ product.description }}</p>
          <p>{{ product.price }}</p>
        </li>
      </ul>
      <!--Table contents-->
      <table>
            <thead>
                <tr>
                    <th>Product ID</th>
                    <th>Product Description</th>
                    <th>Quantity</th>
                    <th>Price</th>
                </tr>
            </thead>
            
        </table>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        products: [
          // Initial products data
        ],
      };
    },
  };
  </script>
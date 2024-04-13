<template>
  <div class="product-list">
    <h2>Product List</h2>
    <table>
      <thead>
        <tr>
          <th>Product Name</th>
          <th>Description</th>
          <th>Price</th>  
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in displayProducts" :key="product.id">
          <td>{{ product.name }}</td>
          <td>{{ product.description }}</td>
          <td>{{ product.price }}</td>
          <td>
          </td>
        </tr>
      </tbody>
    </table>

    
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { id: 1, name: "shoes", description: "Description 1", price: 10, },
        { id: 2, name: "Product 2", description: "Description 2", price: 20,},
        { id: 2, name: "Product 2", description: "Description 2", price: 20,},
        { id: 2, name: "Product 2", description: "Description 2", price: 20,},
        // ...
      ],
      cart: [],
    };
  },
  computed: {
    displayProducts() {
      // Implement a computed property to filter or sort products if needed
      return this.products;
    },
  },
  methods: {
    addToCart(product) {
      this.cart.push(product);
    },
  },
};
</script>

<style>
.product-list {
  font-family: Arial, sans-serif;
  width: 80%;
  margin: auto;
  padding: 2rem;
  border: 1px solid #ddd;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.product-list h2 {
  text-align: center;
  margin-bottom: 1rem;
}

.product-list table {
  width: 100%;
  border-collapse: collapse;
}

.product-list th,
.product-list td {
  padding: 0.5rem;
  border-bottom: 1px solid #ddd;
  text-align: left;
}

.product-list th {
  background-color: #f2f2f2;
  font-weight: bold;
}

.product-list button {
  background-color: #4caf50;
  color: white;
  border: none;
  padding: 0.25rem 0.5rem;
  border-radius: 3px;
  cursor: pointer;
}

.product-list button:hover {
  background-color: #45a049;
}
</style>
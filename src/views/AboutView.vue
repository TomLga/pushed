<template>
  <div class="about">
    <h1>This is an about page</h1>

    <div>
        <h1>Product CRUD</h1>

        <button @click="showAddForm">Add Product</button>

        <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Price</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(product, index) in products" :key="index">
                    <td>{{ product.name }}</td>
                    <td>{{ product.price }}</td>
                    <td>
                        <button @click="editProduct(index)">Edit</button>
                        <button @click="deleteProduct(index)">Delete</button>
                    </td>
                </tr>
            </tbody>
        </table>

        <div v-if="showAddFormFlag">
            <h2>Add Product</h2>
            <label for="productName">Name:</label>
            <input type="text" v-model="newProduct.name"><br>
            <label for="productPrice">Price:</label>
            <input type="number" v-model="newProduct.price"><br>
            <button @click="addProduct">Save</button>
        </div>

        <div v-if="showEditFormFlag">
            <h2>Edit Product</h2>
            <label for="editProductName">Name:</label>
            <input type="text" v-model="editedProduct.name"><br>
            <label for="editProductPrice">Price:</label>
            <input type="number" v-model="editedProduct.price"><br>
            <button @click="updateProduct">Update</button>
            <button @click="cancelEdit">Cancel</button>
        </div>
    </div>


  </div>
</template>



<script>
    const app = Vue.createApp({
        data() {
            return {
                products: [],
                newProduct: { name: '', price: 0 },
                editedProduct: { name: '', price: 0 },
                showAddFormFlag: false,
                showEditFormFlag: false,
                editedProductIndex: null,
            };
        },
        methods: {
            showAddForm() {
                this.showAddFormFlag = true;
            },
            addProduct() {
                if (this.newProduct.name && !isNaN(this.newProduct.price)) {
                    this.products.push({ ...this.newProduct });
                    this.newProduct = { name: '', price: 0 };
                    this.showAddFormFlag = false;
                }
            },
            editProduct(index) {
                this.editedProduct = { ...this.products[index] };
                this.showEditFormFlag = true;
                this.editedProductIndex = index;
            },
            updateProduct() {
                if (this.editedProduct.name && !isNaN(this.editedProduct.price)) {
                    this.products[this.editedProductIndex] = { ...this.editedProduct };
                    this.showEditFormFlag = false;
                }
            },
            cancelEdit() {
                this.showEditFormFlag = false;
            },
            deleteProduct(index) {
                this.products.splice(index, 1);
            },
        },
    });

  
</script>
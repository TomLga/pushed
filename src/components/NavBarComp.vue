<template>
    <nav class="navbar navbar-expand-lg ">
      <div class="container-fluid">
        <img src="https://i.postimg.cc/sfLgCSsg/LT-logo.png" alt="logo" loading="lazy" style="width: 5rem" >
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav  mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link id="linkName" class="nav-link active" aria-current="page" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link id="linkName" class="nav-link active" aria-current="page" to="/about">About</router-link>
            </li>
            <li class="nav-item">
              <router-link id="linkName" class="nav-link active" aria-current="page" to="/admin">Admin</router-link>
            </li>
            <li class="nav-item">
              <router-link id="linkName" class="nav-link active" aria-current="page" to="/products">Products</router-link>
            </li>
            
            <li class="nav-item">
              <router-link id="linkName" class="nav-link active" aria-current="page" to="/contact">Contact</router-link>
            </li>

           </ul>
        </div>
      </div>
    </nav>
    
  </template>
  
  <script>
  export default {
   
  }
  </script>
  
<style>
  .navbar-nav{
    margin: auto;
   
    width: 600px;
    height: 70px;
    border-radius: 20px;

  }
  #linkName{
    margin: auto;
    font-size: 20px;
  }
  .nav-item{
    margin: auto;
  }

  .nav-item:hover{
    text-decoration: underline;
    transform: scale(1.08);
   
    
  }


</style>
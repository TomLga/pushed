<template>
  <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <div class="carousel-text">
          <h1>Kiddies Fashion Watches</h1>
        </div>
        <img src="https://i.postimg.cc/QxvXTBLx/Kids-profile.png" class="d-block w-100" style="height: 40rem" alt="Kids Profile">
      </div>
      <div class="carousel-item">
        <div class="carousel-text">
          <h1 id="mensText">Mens Fashion Watches </h1>
        </div>
        <img src="https://i.postimg.cc/1R2xWLvv/Mens-profile1.jpg" class="d-block w-100" style="height: 40rem" alt="Mens Profile">
      </div>
      <div class="carousel-item">
        <div class="carousel-text">
          <h1>Womens Fashion Watches</h1>
        </div>
        <img src="https://i.postimg.cc/jSqGCt2d/Womens-profile.jpg" class="d-block w-100" style="height: 40rem" alt="Womens Profile">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>

<div class="container-fluid pt-5">
    <div class=" row px-xl-5 pb-3" id="home_icons">
        <div class="col-lg-3 col-md-6 col-sm-12 pb-1" id="home_icons1">
            <div class="d-flex flex-column align-items-center mb-4" >
                <h1 class="fa fa-check text-primary m-0"></h1>
                <i class="bi bi-emoji-heart-eyes fa-10x"></i>
                <h5 class="font-weight-semi-bold m-0">Quality Product</h5>
            </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 pb-1" id="home_icons2">
            <div class="d-flex flex-column align-items-center mb-4">
                <h1 class="fa fa-shipping-fast text-primary m-0"></h1>
                <i class="bi bi-truck"></i>
                <h5 class="font-weight-semi-bold m-0">Free Shipping</h5>
            </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 pb-1" id="home_icons3">
            <div class="d-flex flex-column align-items-center mb-4">
                <h1 class="fa fa-shipping-fast text-primary m-0"></h1>
                <i class="bi bi-arrow-return-left"></i>
                <h5 class="font-weight-semi-bold m-0">10 days return</h5>
              </div>
        </div>
    </div>
</div>


<div class="End line">
    <hr>
  </div> 
  
  <h2 id="ftText">Featured Products</h2>

 <div class="card-group">
  <div class="card">
    <img src="https://i.postimg.cc/cJJJLYsm/Noise-Champ.jpg" class="card-img-top" alt="kids watch" style="width: 17rem; margin:auto">
    <div class="card-body" >
      <h5 class="card-price">R150</h5>
      <button class="seeMoreBtn" type="button">See more</button>
    </div>
  </div>
  <div class="card">
    <img src="https://i.postimg.cc/V6rLj800/Tempo-Pulse-2-0-Smart-watch.jpg" class="card-img-top" alt="womans watch" style="width: 17rem; margin:auto">
    <div class="card-body">
      <h5 class="card-price">R999</h5>
      <button class="seeMoreBtn" type="button">See more</button>
    </div>
  </div>
  <div class="card">
    <img src="https://i.postimg.cc/d0SVk13K/Volkano-Serene-Series.jpg" class="card-img-top" alt="mans watch" style="width: 17rem; margin:auto">
    <div class="card-body">
      <h5 class="card-price">R799</h5>
      <button class="seeMoreBtn" type="button">See more</button>
    </div>
  </div>
</div> 
<button id="seeAllProducts">see all products</button>




  <div class="container-fluid pt-5 pb-3">
    <h2 class="section-title position-relative text-uppercase mx-xl-5 mb-4"></h2>
    <div class="container-fluid">
      <div class="row">
        <div class="col">
            <div class="card products-card" v-for="product in products" :key="product.id">
              <img :src="products.image" class="card-img-top img-fluid" alt="">
              <div class="card-body">
                <h5 class="card-title">{{ products.name }}</h5>
                <a :href="project.url" class="btn btn-primary ">Netlify</a>
                <a :href="project.url1" class="btn btn-primary">Github</a>
              </div>
            </div>
          </div>
        </div>
      </div>
   </div>

</template>

<script>
    export default {
        name: 'HomeView',
        components: {
  
  }
      }

</script>

<style>

#home_icons1,#home_icons2,#home_icons3{

  justify-content: space-between;

  height: 85px;
  font-size: 60px;
  box-shadow: 4px 4px 4px 4px black;
  background: linear-gradient(360deg ,rgb(167, 85, 244), rgba(255, 255, 255, 0.533));
  margin: auto;
  width: 15%;
  
 
}
#home_icons{
  justify-content: space-between;
  border: solid black;
  border-left: none;
  border-right: none;
  border-bottom: none;
  padding: 19px;
 

}

h5{
  font-weight:bolder;
  color: blueviolet;
 
  font-family:Georgia, 'Times New Roman', Times, serif
  
}

/*
 #home_icons2{
    height: 80px;
    justify-content: space-between;
    box-shadow: 4px 4px 4px 4px ;
    background: linear-gradient(40deg ,blueviolet, rgba(255, 255, 255, 0.533));
    width: 990px;
    margin: auto;
}
#home_icons3{
    height: 80px;
    justify-content: space-between;
    box-shadow: 4px 4px 4px 4px ;
    background: linear-gradient(40deg ,blueviolet, rgba(255, 255, 255, 0.533));
    width: 990px;
    margin: auto;
} 
*/
.card-group {
  display: flex;
  justify-content: space-between;
  margin: auto;
}

.card {
  margin: 5%;
  box-shadow: 0px 2px 2px 2px rgb(168, 162, 183);

  
 
  border: none;
}

.card-img-top {

  width: 100%;
  height: auto;
}

.card-body {
  text-align: center;
}
.End-line{
border-bottom: #000 solid 1px;
padding: 130px 0 90px 0;
}



/* logan style */
#ftText{
 font-size: 60px;
 text-align: center;
}

#home_icons1, #home_icons2, #home_icons3{
 background: linear-gradient(rgb(241, 240, 240), rgb(104, 100, 100));
 animation: slideAnimation 6s infinite;
}
@keyframes slideAnimation {
  0% {
    transform: scale(1.15);
  }
  50% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.15);
  }
}


.seeMoreBtn{
  background: linear-gradient(rgb(0, 0, 0), rgb(143, 132, 132));
  color: white;
  width: 120px;
  border-radius: 20px;
}

.card:hover{
  transform: scale(1.15) ;
  box-shadow: 15px 15px rgba(0, 0, 0, 0.493);
}
 #seeAllProducts{
  margin:40px 25%;
  width: 50%;
  height: 2.5rem;
  border-radius: 20px;
  font-style: italic;
  font-size: 20px;
 }
 #seeAllProducts:hover{
  background: linear-gradient(rgb(0, 0, 0), rgb(143, 132, 132));
  color: white;
  text-transform: uppercase;
  
 }

</style>
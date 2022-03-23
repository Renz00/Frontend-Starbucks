<template>
 <div id="content-body">
    <nav class="navbar">
      <div class="navbar-container">
        <div class="navbar-brand">
          <a href="#">
            <img src="@/assets/img/logo.svg" alt="Starbucks logo">
          </a>
        </div>
        <ul class="navbar-nav-left">
          <li><a href="#">Menu</a></li>
          <li><a href="#">Rewards</a></li>
          <li><a href="#">Gift Cards</a></li>
        </ul>
        <ul class="navbar-nav-right">
          <li>
            <a href="#"><img src="@/assets/img/marker.svg" alt="Map marker">
              <span>Find a store</span>
            </a>
          </li>
          <li><a class="btn btn-dark-outline">Sign in</a></li>
          <li><a class="btn btn-dark">Join now</a></li>
        </ul>

        <!--- Hamburger Menu --->

        <button @click="navToggle()" type="button" class="hamburger" id="menu-btn">
          <span class="hamburger-top"></span>
          <span class="hamburger-middle"></span>
          <span class="hamburger-bottom"></span>
        </button>
      </div>
    </nav>

    <!-- Mobile Menu -->
    <div class="mobile-menu hidden" id="menu">
      <ul>
           <li><a href="#">Menu</a></li>
          <li><a href="#">Rewards</a></li>
          <li><a href="#">Gift Cards</a></li>
      </ul>
      <div class="mobile-menu-bottom">
        <button class="btn btn-dark-outline">
          Sign  in
        </button>
        <button class="btn btn-dark">Join now</button>
        <div>
          <a href="#"><img src="@/assets/img/marker.svg" alt="Map marker">
            <span>Find a store</span>
          </a>
        </div>
      </div>
    </div>

    <!-- Content Box A -->
    <section class="box box-a bg-primary text-center py-md">
      <div class="box-inner">
        <h2 class="text-xl">Jingle all the way to free favorites</h2>
        <p class="text-md">
          Join Starbucks Rewards for delicious deals &amp; exclusive offers.
          <a href="#">Learn more</a>
        </p>
      </div>
    </section>
    
    <!-- Content Box B -->
    <section class="box box-b bg-secondary grid-col-2">
      <img src="@/assets/img/box-b.png" alt="Content box 2">
      <div class="box-text">
        <h2 class="text-xl">Lorem ipsum dolor sit amet.</h2>
        <p class="text-md">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Est, aperiam?</p>
        <a href="#" class="btn btn-light-outline">Order now</a>
      </div>
    </section>

    <!-- Content Box c -->
    <section class="box box-c bg-secondary grid-col-2 grid-reversed">
      <img src="@/assets/img/box-c.png" alt="Content box c">
      <div class="box-text">
        <h2 class="text-xl">Lorem ipsum dolor sit amet.</h2>
        <p class="text-md">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolore architecto, nemo praesentium soluta repellat eum.</p>
        <a href="#" class="btn btn-light-outline">Order now</a>
      </div>
    </section>

    <!-- Content Box d -->
    <section class="box box-d bg-primary grid-col-2">
      <img src="@/assets/img/box-d.png" alt="Content box d">
      <div class="box-text">
        <h2 class="text-xl">Lorem ipsum dolor sit amet consectetur adipisicing.</h2>
        <p class="text-md">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae beatae minus ullam.</p>
        <a href="#" class="btn btn-light-outline">Order now</a>
      </div>
    </section>

     <!-- Content Box e -->
    <section class="box box-e bg-secondary grid-col-2 grid-reversed">
      <img src="@/assets/img/box-e.jpg" alt="Content box e">
      <div class="box-text">
        <h2 class="text-md">Lorem ipsum dolor sit amet.</h2>
        <p class="text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolorem quibusdam neque nemo nesciunt sint placeat commodi dolore aut?</p>
        <a href="#" class="btn btn-light-outline">Order now</a>
      </div>
    </section>

    <!-- Content Box F -->
    <section class="box box-f grid-col-2">
      <div>
          <img src="@/assets/img/box-f1.jpg" alt="Content box e">
          <div class="bg-extra py-lg">
              <div class="box-text">
              <h2 class="text-md">Lorem ipsum dolor sit amet.</h2>
              <p class="text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolorem quibusdam neque nemo nesciunt sint placeat commodi dolore aut?</p>
              <a href="#" class="btn btn-dark-outline">Order now</a>
            </div>
          </div>   
      </div>
       <div>
          <img src="@/assets/img/box-f2.jpg" alt="Content box e">
          <div class="bg-primary py-lg">
              <div class="box-text">
                <h2 class="text-md">Lorem ipsum dolor sit amet.</h2>
                <p class="text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolorem quibusdam neque nemo nesciunt sint placeat commodi dolore aut?</p>
                <a href="#" class="btn btn-light-outline">Order now</a>
              </div>
          </div>
      </div>
    </section>

    <div class="divider">
      <footer class="footer">
        <div class="footer-container">
          <div class="social">
             <a href="https://spotify.com">
            <img src="@/assets/img/social-spotify.svg" alt="" />
          </a>
          <a href="https://facebook.com">
            <img src="@/assets/img/social-facebook.svg" alt="" />
          </a>
          <a href="https://pinterest.com">
            <img src="@/assets/img/social-pinterest.svg" alt="" />
          </a>
          <a href="https://instagram.com">
            <img src="@/assets/img/social-instagram.svg" alt="" />
          </a>
          <a href="https://youtube.com">
            <img src="@/assets/img/social-youtube.svg" alt="" />
          </a>
          <a href="https://twitter.com">
            <img src="@/assets/img/social-twitter.svg" alt="" />
          </a>
          </div>
          <p>© 2021 Starbucks Coffee Company. All rights reserved.</p>
        </div>
      </footer>
    </div>
 </div>
</template>

<script>
  export default {
    data: () => ({
    }),
    methods: {
      navToggle (){
        const btn = document.getElementById('menu-btn')
        const nav = document.getElementById('menu')
        
        btn.classList.toggle('open')// add a class named 'open' to the btn element
        nav.classList.toggle('hidden')
      
        this.$root.$emit('toggleNoScroll') //calling a method inside another component (App.vue)
      }
    }
  }
</script>

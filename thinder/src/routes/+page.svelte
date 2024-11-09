<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger} from 'flowbite-svelte';
</script>
<Navbar class="nav">
  <NavBrand href="/">
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Thinder</span>
  </NavBrand>
  <NavHamburger />
  <NavUl>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/login">Log in</NavLi>
      <NavLi href="/signup">Sign up</NavLi>
  </NavUl>
</Navbar>

<main>
    <header>
      <h1>Welcome to Thinder!</h1>
      <p>Here you can be protected by our complex encryption system and feel loved and accepted! ❤️</p>
      <section class= "image">
       
        <img src="/image.jpg" alt="img"
        width={500}
        height={700}
        />
       
        </section>
    </header>
   
    <section class="intro">
      <h2>About us:</h2>
      <u1>
      <p>Our goal is to make you feel better about anything bothering you and
        getting the help you need! We offer extensive services make you feel at
        home in our wonderful feedback environment. If you have any immediate thoughts
        of self-harm, please contact number 988. Otherwise, use our web page for seeking
        better help from our professional therapists that we offer on our site.
      </p>
     </u1>
    </section>
 
    <section class="features">
      <h2>How it works:</h2>
      <ul>
        <p>INSERT HOW IT WORKS HERE</p>
       
      </ul>
    </section>
 
    <div class="button-cont">
        <button>
            <p>Button goes here</p>
        </button>
    </div>
  </main>
 
 
 

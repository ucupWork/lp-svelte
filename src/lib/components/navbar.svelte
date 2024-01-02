  <script>
	import Logo from '../assets/logo/logo-black.png'
	import { page } from '$app/stores';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	$: activeUrl = $page.url.pathname;
	let activeClass = 'text-white underline underline-offset-1 bg-neutral-400 md:bg-transparent md:text-neutral-600';
	let nonActiveClass = 'text-gray-700 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-neutral-700';
  </script>
  
  <Navbar class='p-6'>
	<NavBrand href="/">
	  <img src={Logo} class="me-3 h-10 lg:h-16 sm:h-9" alt="Flowbite Logo" />
	</NavBrand>
	<NavHamburger />
	<NavUl {activeUrl} {activeClass} {nonActiveClass}>
	  <NavLi href="/">Home</NavLi>
	  <NavLi href="/products">Products</NavLi>
	  <NavLi href="/kalkulator">Kalkulator</NavLi>
	  <NavLi href="/blog">Blog</NavLi>
	  <NavLi href="/resep">Resep</NavLi>
	</NavUl>
  </Navbar>
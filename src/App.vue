<script setup>
</script>

<template>
  
  <div class="blog">
    <div class="blog-part is-menu">
      <a href="/" class="blog-menu">
        Home
        <svg fill="none" stroke="currentColor" stroke-width=".7" stroke-linecap="round" stroke-linejoin="round"
        class="feather feather-arrow-up-right" viewBox="0 0 24 24">
        <path d="M7 17L17 7M7 7h10v10" />
      </svg>
    </a>
    <a href="/about" class="blog-menu">About Me</a>
    <a href="/message" class="blog-menu">Messages</a>
    <a href="/contact" class="blog-menu">Contact</a>
    <a href="#" class="blog-menu mention">@stemmet_</a>
    <a href="/login" class="blog-menu subscribe">Login/Register</a>
  </div>
  <RouterView/>
  </div>
</template>

<style>
 * {
	 outline: none;
	 box-sizing: border-box;
}
 html {
	 box-sizing: border-box;
	 -webkit-font-smoothing: antialiased;
}
 img {
	 max-width: 100%;
}
 body {
	 background-color: #D2C9AA;
	 display: flex;
	 font-family: "Inter", sans-serif;
	 justify-content: center;
	 align-items: center;
	 flex-direction: column;
	 width: 100%;
	 font-weight: 400;
	 height: 100vh;
   overflow: hidden;
}
 @media screen and (max-width: 768px) {
	 body {
		 padding: 0;
	}
}

/* MAIN ARTICLE */

 .blog {
	 background-color: #D2C9AA;
	 max-width: 100vw;
	 display: grid;
	 height: 100vh;
	 overflow: hidden;
	 grid-template-columns: 15% 20% 40% 25%;
	 grid-template-rows: 100%;
	 width: 100%;
	 padding: 40px 4px;
	 position: relative;
}
 @media screen and (max-width: 1030px) {
	 .blog {
		 grid-template-columns: 20% 50% 30%;
	}
}
 @media screen and (max-width: 768px) {
	 .blog {
		 grid-template-columns: 25% 75%;
		 width: 100%;
		 max-width: none;
	}
}
 @media screen and (max-width: 560px) {
	 .blog {
		 grid-template-columns: 100%;
	}
}
 .blog-part {
	 padding: 0 20px;
}
 .blog-part:not(:last-child) {
	 border-right: 1px solid #94918f;
}

/* MENU */
 .blog-menu {
	 font-size: 22px;
	 text-decoration: none;
	 color: #161419;
	 display: flex;
	 letter-spacing: -0.5px;
	 align-items: center;
}
 @media screen and (max-width: 1260px) {
	 .blog-menu {
		 font-size: 1.6vw;
	}
}
 .blog-menu svg {
	 width: 22px;
	 margin-left: 4px;
}
 .blog-menu + .blog-menu {
	 margin-top: 24px;
}
 .blog-menu.mention {
	 margin-top: auto;
	 font-size: 19px;
}
 @media screen and (max-width: 1260px) {
	 .blog-menu.mention {
		 font-size: 1.4vw;
	}
}
 .blog-menu.subscribe {
	 margin-top: 8px;
	 font-size: 19px;
	 position: relative;
}
 @media screen and (max-width: 1260px) {
	 .blog-menu.subscribe {
		 font-size: 1.4vw;
	}
}
 .blog-menu.subscribe:before {
	 content: "";
	 width: 16px;
	 height: 16px;
	 background-color: #161419;
	 left: 0;
	 border-radius: 1px;
	 margin-right: 14px;
}
 .blog-menu.rounded:before {
	 content: "";
	 border-radius: 50%;
	 width: 12px;
	 height: 12px;
	 background-color: #161419;
	 margin-right: 12px;
}
 .blog .is-menu {
	 display: flex;
	 flex-direction: column;
}
 @media screen and (max-width: 1030px) {
	 .blog .is-menu {
		 display: none;
	}
}
</style>
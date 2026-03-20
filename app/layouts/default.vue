<template>
<header>
	<div class="menu">
		<ul class="menu-items">
			<li class="menu-item">
				<img class="logo" src="/logo/pt_color.png">
			</li>
			<div class="items-flex">
				<li class="menu-item">
					<NuxtLink to="/about">About</NuxtLink>
				</li>
				<li class="menu-item">
					<NuxtLink to="/contact">Contact</NuxtLink>
				</li>
				<!-- <li class="menu-item">Upcoming events</li> -->
				<!-- <li class="menu-item">
					<NuxtLink to="/discography">Discography</NuxtLink>
				</li> -->
			</div>
		</ul>
	</div>
</header>
<div class="container">
	<div class="main">
		<slot></slot>
	</div>
	<footer>
		<div class="socials">
			<!-- <a href="" target="_blank" class="social-icon" aria-disabled>
				<img src="/vectors/youtube.svg">
			</a> -->
			<a href="https://www.instagram.com/partytuuri" target="_blank" class="social-icon" aria-disabled>
				<img src="/vectors/instagram.svg" height="16px">
			</a>
			<!-- <a href="" target="_blank" class="social-icon" aria-disabled>
				<img src="/vectors/soundcloud.svg">
			</a> -->
		</div>	
		<p>All rights reserved © {{ currentYear }}</p>
		<p class="website-by">Website by <a href="https://vilts.ch" target="__blank">vilts</a></p>
	</footer>
</div>
</template>

<script setup>
const currentYear = new Date().getFullYear();

useHead({
	titleTemplate: (title) => {
		return title ? `${title} | Partytuuri Orchestra` : 'Partytuuri Orchestra';
	}
})

useSeoMeta({
	ogTitle: 'Partytuuri Orchestra',
	description: 'Partytuuri Orchestra - A SHARED EXPERIENCE ABOUT BREAKING THE RULES SERVING YOU MUSIC IN UNTRADITIONAL WAYS.',
	ogDescription: 'Partytuuri Orchestra - A SHARED EXPERIENCE ABOUT BREAKING THE RULES SERVING YOU MUSIC IN UNTRADITIONAL WAYS.'
})
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200..900&display=swap');

html, body {
	background: black;
	color: white;
	min-width: fit-content;
	font-family: "Inconsolata", monospace;
}

.menu {
	margin-bottom: 36px !important;
}

a {
	color: white;
	text-decoration: none;
}

.container {
	min-height: 70vh;    
    display: flex;
    flex-direction: column;
	margin-top: 150px;
	line-height: 100%;
}

@media (max-width: 700px) {
	.container {
		margin-top: 36px;
	}
}

.items-flex {
	display: flex;
    gap: 36px;
}

.socials {
	margin-top: 24px;
	margin-bottom: 24px;
	display: flex;
	justify-content: center;
	gap: 24px;
}

.social-icon img {
	height: 24px;
}

.social-icon:hover {
	filter: opacity(var(--value, 80%));
	transition: filter .3s;
}

a.router-link-active {
	text-decoration: underline;
}

a:hover {
	text-decoration: underline;
}

.logo {
	/* filter: invert(1); */
	margin: auto;
	padding: unset;
	width: 200px;
}

ul li {
	list-style-type: none;
}

@media (max-width: 700px) {
	.menu-items {
		flex-direction: column;
	}
	.items-flex {
		justify-content: space-between;
	}
}

div.menu .menu-items {
	display: flex;
	justify-content: space-between;
	font-size: 24px;
	position: fixed;
	width: 100%;
	top: 0;
	left: 0;
	padding: 12px;
}

@media (max-width: 700px) {
	div.menu .menu-items {
		position: relative;
	}
}

.menu-item {
	cursor: pointer;
}

.main {
	/* max-width: 700px; */
	margin: auto;
	width: 100%;
}

footer p {
	opacity: 60%;
	font-size: 12px;
	color: #EAEFEF;
}

p.website-by {
	font-size: 8px;
	margin-top: 12px;
}

footer {
	margin-top: 60px;
	border: none;
	margin-bottom: 24px;
}
</style>

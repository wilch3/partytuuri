<template>
<div class="about-layout">
	<div class="about">
			<p class="bigger-text">A SHARED EXPERIENCE ABOUT BREAKING THE RULES - SERVING YOU MUSIC IN UNTRADITIONAL WAYS.</p>
  			<div class="p-separator"></div>
  			<div class="p-separator"></div>
			<p>It all began when our group of friends consisting of young musicians got frustrated in the stiff etiquette in the classical music world. Realizing the lack of interest and the loss of livelihood in our promised audience urged us to take action: to break out from the traditions. We refuse to be slowed down, and instead created an alternative.</p>
  			<div class="p-separator"></div>
			<p>Partytuuri Orchestra delivers symphonic hits adjusted to serve the club scene. In addition to respecting the origin of the art, we wanted to bring the evergreen pieces out of the velvety concert halls - for them to be accessible, and for everyone to enjoy! We invite you to celebrate our cross-genre fusion project where you get to witness Stravinsky, Vivaldi and Brahms (among other legends) hitting the dance floor. The mission of our orchestra is to employ young musicians who share the spirit and ambition of our project!</p>
			<div class="p-separator"></div>
			<div class="p-separator"></div>
			<p class="bigger-text">WE FIND IT ACCEPTABLE TO PARTY TO VIVALDI.</p>
	</div>
	<div class="events-block">
		<div>
			<h4 class="upcoming-events">upcoming events</h4>
			<div v-for="i in 1" class="event-item">
				<p class="name">Partytuuri Orchestra x Helsingin Oopperakesä</p>
				<p class="date">28.8.2026 20:30–22:00<span>&#x2022;</span> Teurastamon Piha</p>
				<a class="event-link" href="https://teurastamo.com/tapahtumat/partytuuri-orchestra-x-helsingin-oopperakesa/" target="_blank"><i>event page</i></a>
			</div>
		</div>
		<div>
			<h4 class="past-events">past events</h4>
			<div v-for="i in 1" class="event-item">
				<p class="name">PARTYTUURI ORCHESTRA</p>
				<p class="date">15.4.2026 <span>&#x2022;</span> Musiikkitalo (Black Box)</p>
			</div>
		</div>
	</div>
</div>
</template>

<script setup lang="ts">
useHead({
	title: 'About',
	meta: [
		{ name: 'description', content: 'About Partytuuri Orchestra' }
	],
})

useHead({
	meta: [{ property: 'og:title', content: `About Partytuuri Orchestra` }]
})
</script>

<style lang="css">
.bigger-text {
	font-weight: bold;
    font-size: 20px;
    line-height: 120%;
}
.p-separator {
	display: block;
	padding: 8px;
}
.about-layout {
	display: grid;
	grid-template-columns: 1fr 1fr;
}
@media (max-width: 700px) {
	.about-layout {
		grid-template-columns: 1fr;
	}
	.upcoming {
		margin-top: 60px !important;
		text-align: left !important;
	}
	.upcoming-event {
		font-size: 14px !important;
	}
}
.events-block {
	text-align: right;
	gap: 48px;
	display: flex;
	flex-direction: column;
}
.event-link {
	text-transform: lowercase;
	font-size: 10px;
}
.event-item {
	margin-bottom: 8px;
	display: flex;
	flex-direction: column;
	gap: 8px;
}
.name {
	font-size: 20px;
}
.upcoming-events {
	color: #a5efdb;
}
.past-events {
	opacity: 50%;
}
.upcoming-events, .past-events {
	font-size: 10px;
	text-transform: uppercase;
	margin-bottom: 12px;
}
.date {
	font-size: 14px;
	opacity: 80%;
}
</style>
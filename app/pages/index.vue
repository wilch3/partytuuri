<template>
<NuxtLayout :name="layout">
	<NuxtPage />
</NuxtLayout>
</template>

<script setup lang="ts">
const layout = 'default'

await navigateTo('/about')
</script>

<style lang="css">
body {
	width: 100%;
    min-width: fit-content;
}

ul li {
	list-style-type: none;
}
div.menu .menu-items {
	display: flex;
	justify-content: space-between;
	font-size: 24px;
	padding: unset;
}

.menu-item {
	cursor: pointer;
}

.main {
	/* max-width: 700px; */
	margin: auto;
}
</style>
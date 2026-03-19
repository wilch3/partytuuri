<script setup>
defineProps({ blok: Object });
</script>

<template>
	<div class="feature" v-editable="blok">
		<span>Test</span>
		<span>{{ blok.name }}</span>
	</div>
</template>

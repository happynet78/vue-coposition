<template>
	<h2>Chilc Component B</h2>
	<ChildC />
</template>

<script>
import ChildC from './ChildC.vue'

	export default {
		name: 'ChildB',
		components: {
			ChildC,
		},
	}
</script>

<style scoped>

</style>
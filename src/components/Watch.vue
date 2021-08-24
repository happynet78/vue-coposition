<template>
	<div>
		<!-- Options API -->
		<input type="text" placeholder="Name" v-model="name" />

		<!-- ref -->
		<input type="text" placeholder="First Name" v-model="firstName" />
		<input type="text" placeholder="Last Name" v-model="lastName" />

		<!-- reactive -->
		<input type="text" placeholder="Reactive First Name" v-model="fName" />
		<input type="text" placeholder="Reactive Last Name" v-model="lName" />
		<input type="text" placeholder="Reactive Hero Name" v-model="options.heroName" />
	</div>
</template>

<script>
import { ref, reactive, toRefs, watch } from 'vue'
import _ from 'lodash'

	export default {
		name: 'Watch',
		setup() {
			const state = reactive({
				fName: '',
				lName: '',
				options: {
					heroName: '',
				},
			})

			// watch(
			// 	() => {
			// 		return {...state}
			// 	}, function(newValue, oldValue) {
			// 	console.log('fName Old Value', oldValue.fName)
			// 	console.log('fName New Value', newValue.fName)
			// 	console.log('fName Old Value', oldValue.lName)
			// 	console.log('fName New Value', newValue.lName)
			// }) 

			watch(
				() => _.cloneDeep(state.options), 
				function(newValue, oldValue) {
					console.log('fname Old value', oldValue)
					console.log('fname New value', newValue)
				},
				{
					deep: true,
				}
			)

			const firstName = ref('')
			const lastName = ref('')

			watch(
				[firstName, lastName],
				function(newValues, oldValues) {
					console.log('FirstName Old Value', oldValues[0])
					console.log('LastName New Value', newValues[0])

					console.log('LastName Old Value', oldValues[1])
					console.log('LastName New VAlue', newValues[1])
				},
				{
					immediate: true,
				}
			)

			return {
				firstName,
				lastName,
				...toRefs(state)
			}
		},
		data() {
			return {
				name: '',
			}
		},
		watch: {
			name(newValue, oldValue) {
				console.log('oldValue', oldValue)
				console.log('newValue', newValue)
			},
		},
	}
</script>

<style scoped>

</style>
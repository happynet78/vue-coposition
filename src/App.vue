<template>
	<Data />
	<DemoOne />
	<DemoTwo />
	<Methods />
	<VModel />
	<Computed />
	<Watch />
	<ProvideInject />
	<LifeCycleO />
	<LifeCycleC />
	<TemplateRef />
	<Person />
	<ClickCount />
	<HoverCount />
</template>

<script>
import Data from './components/Data.vue'
import DemoOne from './components/DemoOne.vue'
import DemoTwo from './components/DemoTwo.vue'
import Methods from './components/Methods.vue'
import VModel from './components/VModel.vue'
import Computed from './components/Computed.vue'
import Watch from './components/Watch.vue'
import ProvideInject from './components/ProvideInject.vue'
import LifeCycleO from './components/LifecycleO.vue'
import LifeCycleC from './components/LifecycleC.vue'
import TemplateRef from './components/TemplateRef.vue'
import Person from './components/Person.vue'
import ClickCount from './components/ClickCounter.vue'
import HoverCount from './components/HoverCounter.vue'

export default {
	name: 'App',
	components: {
		Data,
		DemoOne,
		DemoTwo,
		Methods,
		VModel,
		Computed,
		Watch,
		ProvideInject,
		LifeCycleO,
		LifeCycleC,
		TemplateRef,
		Person,
		ClickCount,
		HoverCount,
	}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
	<div>
		<img alt="Need a GUID?" src="../assets/need-a-guid.png" class="img-fluid" />
		<div>
			<v-btn v-on:click="generateGuid()" color="primary">Generate a GUID</v-btn>
			<div>
				<span>{{ guid }}</span>
			</div>
		</div>
	</div>
</template>

<script>
import { uuid } from 'vue-uuid'

export default {
	name: 'GuidMan',
	data() {
		return {
			guid: null
		}
	},
	methods: {
		generateGuid() {
			this.guid = uuid.v4().toUpperCase()
		}
	}
}
</script>

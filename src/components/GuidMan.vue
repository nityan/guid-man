<template>
	<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12 col-12">
		<img alt="Need a GUID?" src="../assets/need-a-guid.png" class="img-fluid" />
		<div>
			<button class="btn btn-primary" v-on:click="generateGuid()">Generate a GUID</button>
		</div>
		<span>{{ guid }}</span>
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

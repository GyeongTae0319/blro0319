<template>
	<div class="post-block-subheading">
		<div class="block">
			<span>{{ value.value.content }}</span>
		</div>
	</div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

@Component
export default class PostBlockSubheading extends Vue {
	@Prop({
		type: Object,
		required: true
	}) value!: { [key: string]: any };
	@Prop({
		type: Vue,
		required: true
	}) bus!: Vue;
}
</script>

<style lang="scss" scoped>
@import "../../../assets/styles/variables";

.post-block-subheading {
	padding: {
		top: 15px;
		bottom: 16px;
	};

	.block {
		padding: 0 32px;
		font-size: x-large;
	}
}
</style>

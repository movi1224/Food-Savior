<template>
	<div class="header-bar">
		<router-link to="/"> <i class="bi bi-house-door homeIcon"></i></router-link>

		<div class="leftPart">
			<div class="rewardPart">
				<img class="chiefIcon" :src="chiefIcon" />
				<p style="font-weight: bold; vertical-align: middle; display: inline; position: relative; top: 2px;"><i class="el-icon-close
" style="margin-left:1px"></i> {{ this.rewardPoints }}</p>
			</div>
			<div style="vertical-align: middle; display: inline">
				<router-link to="/reward">
					<i class="bi bi-person-circle personIcon"></i>
				</router-link>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'HeaderBar',
	data() {
		return {
			icon: require('/src/assets/logo_food_savior.jpg'),
		};
	},
	mounted: function () {},
	methods: {},
};
</script>
<style>
.chiefIcon {
	width: 30px;
	height: 30px;
}
.personIcon,
.homeIcon {
	font-size: 25px;
}
.rewardPart {
	display: inline-block;
	width: 100px;
	position: relative;
	top: -2px;
}
</style>

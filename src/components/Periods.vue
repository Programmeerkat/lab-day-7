<template>
	<v-row>
        <v-col cols="12">
			<v-card>
				<v-tabs
				v-model="tab"
				bg-color="blue"
				align-tabs="left"
				>
				<v-tab value="weeks">Weeks</v-tab>
				<v-tab value="months">Months</v-tab>
				</v-tabs>

				<v-card-text>
				<v-window v-model="tab">
					<v-window-item value="weeks" class="text-left">
						<WeekComponent :weekdata="weekdata"/>
					</v-window-item>

					<v-window-item value="months" class="text-left">
					months
					</v-window-item>
				</v-window>
				</v-card-text>
			</v-card>
		</v-col>
    </v-row>
</template>

<script>
import WeekComponent from './WeekComponent.vue'

	export default {
		// eslint-disable-next-line vue/multi-word-component-names
		name: "Periods",
		components: { WeekComponent },
		data: () => ({
			tab: null,
			weekdata: [
				{
					day: "Mon",
					date: "01-01-2023",
					hours: "8",
				},
				{
					day: "Tue",
					date: "02-01-2023",
					hours: "8",
				},
				{
					day: "Wed",
					date: "03-01-2023",
					hours: "8",
				},
				{
					day: "Thu",
					date: "04-01-2023",
					hours: "8",
				},
				{
					day: "Fri",
					date: "05-01-2023",
					hours: "8",
				},
				{
					day: "Sat",
					date: "06-01-2023",
					hours: "8",
				},
				{
					day: "Sun",
					date: "07-01-2023",
					hours: "8",
				},
			]
		}),
	};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

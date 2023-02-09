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
						<WeekComponent />
					</v-window-item>
					<v-window-item value="months" class="text-left">
						<div v-for="month in months" :key="month">
							<MonthComponent :month="month.slice(0, 3)" />
						</div>
					</v-window-item>
				</v-window>
				</v-card-text>
			</v-card>
		</v-col>
    </v-row>
</template>

<script>
import WeekComponent from './WeekComponent.vue'
import MonthComponent from './MonthComponent.vue'

	export default {
		// eslint-disable-next-line vue/multi-word-component-names
		name: "Periods",
		components: {
			WeekComponent,
			MonthComponent
		},
		data: () => ({
			tab: null,
			months: [
				"January",
				"February",
				"March",
				"April",
				"May",
				"June",
				"July",
				"August",
				"September",
				"October",
				"November",
				"December"
			]
		})
	};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

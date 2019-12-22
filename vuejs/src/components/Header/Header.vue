<template>
	<div class="header-wrapper">
		<div class="date-wrapper">
			<div class="day">
				{{today.getDate()}}
			</div>
			<div class="date-inner-wrapper">
				<div class="month">
					{{monthNames[today.getMonth()]}}
				</div>
				<div class="year">
					{{today.getFullYear()}}
				</div>
			</div>
		</div>
		<div class="day-name">
			{{dayNames[today.getDay()]}}
		</div>
	</div>
</template>

<script>
	const monthNames = [ "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec" ];
	const dayNames = [ "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday" ];

	export default {
		name: "Header",
		data: () => ({
			monthNames: monthNames,
			dayNames: dayNames,
			today: new Date()
		})
	};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.header-wrapper {
        display: grid;
        grid-template-columns: 110px 1fr auto;
        padding: 40px;
    }
    .date-wrapper {
        display: grid;
        grid-template-columns: 55px 45px;
        column-gap: 5px;
        height: 58px;
    }
    .day {
        text-align: center;
        font-size: 45px;
        color: #FF00FF;
    }
    .date-inner-wrapper {
        display: grid;
        grid-auto-rows: 1fr;
        padding: 8px 0 5px 0;
    }   
    .day-name {
        grid-column: 3/4;
        padding-top: 12px;
        font-size: 26px;
    }
</style>

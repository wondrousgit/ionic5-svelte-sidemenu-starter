<ion-header>
	<ion-toolbar>
		<ion-buttons slot="start">
		<ion-menu-toggle>
			<ion-button  color='primary'>
			<ion-icon slot="icon-only" name={icon}></ion-icon>
			</ion-button>
		</ion-menu-toggle>
		</ion-buttons>
		<ion-title>{label}</ion-title>
	</ion-toolbar>
</ion-header>

<script lang='ts'>
    export let label:string;
    export let icon :string 
</script>
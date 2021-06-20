<script lang='ts'>
	import Router,{link} from 'svelte-spa-router'

	const Pages:Array<{url:string,componet:any,label:string,icon:string}> =[]



	import Inbox from './pages/inbox.svelte'
	Pages.push( { url:'/inbox',componet:Inbox,label:'Inbox',icon:'mail' } )



	import Outbox from './pages/outbox.svelte'
	Pages.push( { url:'/outbox',componet:Outbox,label:'Outbox',icon:'heart' } )



	//routes for Router from svelte-spa-router
	const routes={};

	Pages.forEach( page=>{
		routes[page.url] = page.componet
	})



	//set the default page
	routes['/'] = Inbox


</script>


<ion-app>
	<ion-menu content-id="this_id_should_always_as_same_as_ion-menu_in_App_svelte">

		<ion-header>
			<ion-toolbar color="primary">
				<ion-title>Ionic5 Svelte  </ion-title>
			</ion-toolbar>
		</ion-header>

		<ion-content>
			<ion-list>
				<ion-list-header>SideMenu</ion-list-header>

				{#each Pages as page}
					<ion-menu-toggle auto-hide="false">
						<ion-item button>
							<ion-icon slot="start" name={page.icon}></ion-icon>
							<a href={page.url} class='item-native' use:link >{page.label}</a>
						</ion-item>
					</ion-menu-toggle>
				{/each}

			</ion-list>
		</ion-content>
	</ion-menu>


	<Router {routes}/>

</ion-app>

<style>
	a{
		width:100%;
		height:100%;
		line-height: 3rem;
		display: inline-block;
		text-align: left;
		text-decoration: none;
		color:black;
	}
</style>
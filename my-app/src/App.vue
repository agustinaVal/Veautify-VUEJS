<template>
	<div>
	
    <v-toolbar color="pink" dark>
			<v-app-bar-nav-icon></v-app-bar-nav-icon>

			<span class="subheading">App Vuetify</span>

			<v-spacer></v-spacer>

			<v-toolbar-items class="hidden-sm-and-down">
				<v-btn text>
					Inicio
				</v-btn>

				<v-divider vertical></v-divider>

				<v-btn text>
					Buscar
				</v-btn>

				<v-divider vertical></v-divider>

				<v-btn text>
					Acerca de
				</v-btn>
			</v-toolbar-items>
		</v-toolbar>
    
  
		<Cartas />
	</div>
</template>

<script>
import Cartas from '@/components/Cartas.vue';
export default {
	name: 'App',

	components: {
		Cartas,
	},

	data: () => ({
		//
	}),
};
</script>

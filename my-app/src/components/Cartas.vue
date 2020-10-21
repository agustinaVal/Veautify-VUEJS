<template>
	<v-app>
		<v-container>
			<v-main>
				<v-row>
                <v-col md="4" v-for="(personaje, i) in personajes" :key="i">
                <v-card  class="mx-auto" max-width="344">
					<v-img :src="personaje.imagen" height="200px"></v-img>

					<v-card-title>
						{{personaje.nombre}}
					</v-card-title>

					<v-card-actions>
						<v-btn color="orange lighten-2" text>
							Descripción
						</v-btn>

						<v-spacer></v-spacer>

						<v-btn icon @click="personaje.show = !personaje.show">
							<v-icon>{{ personaje.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
						</v-btn>
					</v-card-actions>

					<v-expand-transition>
						<div v-show="personaje.show">
							<v-divider></v-divider>

							<v-card-text>
							{{personaje.description}}
							</v-card-text>
						</div>
					</v-expand-transition>
				</v-card>
                </v-col>
                </v-row>
			</v-main>
		</v-container>
	</v-app>
</template>

<script>
export default {
	data: () => ({
		personajes: [
			{
				id: 1,
				nombre: 'Morty',
                imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg',
                show: false,
                description: 'Morty Smith es uno de los personajes principales de la serie Rick y Morty, del canal de televisión animado Adult Swim. Creado por Justin Roiland y Dan Harmon, Morty es un nervioso adolescente basado en Marty McFly de Regreso al Futuro.'
			},
			{
				id: 2,
				nombre: 'Rick',
                imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg',
                show: false,
                description: 'Rick Sánchez es el personaje principal de la serie de animación de Adult Swim, Rick y Morty. Creado por Justin Roiland y Dan Harmon, Rick es un brillante científico alcohólico. Sánchez es un científico que tiene grandes aventuras con su nieto Morty.'

			},
			{
				id: 3,
				nombre: 'Summer',
                imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg',
                show: false,
                description: 'Summer Smith es la hija mayor de Jerry y Beth. Es la única en enterarse de que el Morty y el Rick son de otra dimensión (Dimensión C-137) y que los de su dimensión (desconocida aún) habían muerto.'
			},
			{
				id: 4,
				nombre: 'Beth',
                imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg',
                show: false,
                description: ' Es la hija de Rick pero técnicamente es la hija de un Rick muerto en un accidente, a lo que el Rick y Morty originarios de la Dimensión C-137 ocuparon sus lugares. Es la esposa de Jerry y la madre de Summer y de Morty (quién murió en el mismo accidente que Rick).'
			},
			{
				id: 5,
				nombre: 'Jerry',
                imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg',
                show: false,
                description: 'Jerry Smith es el esposo de Beth Smith, además es el padre de Summer Smith y Morty Smith.'
			},
		],
	}),
};
</script>

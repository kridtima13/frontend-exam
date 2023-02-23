<template>
	<v-app dark>
		<v-container>
			<v-toolbar flat color="transparent" height="150">
				<img src="kindpng.png" alt="Vuetify.js" height="80">

				<v-toolbar-title class="mx-1 font-italic text-uppercase font-bold-italic" v-text="'lorem'"></v-toolbar-title>
				<v-toolbar-title class="mx-1 font-italic text-uppercase font-bold-italic" v-text="'ipsum'" style="color: #D9EF0C"></v-toolbar-title>              

				<v-toolbar-items style="height: 0" class="ml-10 pl-10">
					<v-btn text class="font-light text-uppercase">lorem</v-btn>
					<v-btn text class="font-light text-uppercase">
						lorem 
						<v-icon class="ml-0" small right>mdi-chevron-down</v-icon>
					</v-btn>
					<v-btn text class="font-light text-uppercase">loremipsum</v-btn>
					<v-btn text class="font-light text-uppercase">lorem & ipsum</v-btn>
					<v-btn text class="font-light text-uppercase">lorem</v-btn>
				</v-toolbar-items>
			</v-toolbar>
		</v-container>

		<v-main>
			<section>
				<v-container >
					<v-row  class="mt-12" align="center" justify="center">
						<v-col class="px-12" cols="12" sm="12" md="5" lg="5" xl="5" align="left">
							<span class="text-uppercase font-bold" style="font-size: 96px; line-height: normal;">LoREM
								<span class="text-uppercase font-bold" style="color: #D9EF0C;">IPSUM</span>
							</span>
							
							<br><br><br><br>
							<span class="font-medium" style="font-size: 20px">Lorem Ipsum is simply Lorem Ipsum is simply Lorem Ipsum is simply</span>
							<br><br>
							<span class="font-light" style="font-size: 18px">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's </span>
						</v-col>

						<v-col cols="12" sm="12" md="7" lg="7" xl="7" align="center">
							<v-img src="Bicycle.png" lazy-src="Bicycle.png" contain height="504" width="858">
								<template v-slot:placeholder>
									<v-row class="fill-height ma-0" align="center" justify="center">
										<v-progress-circular color="grey lighten-5"></v-progress-circular>
									</v-row>
								</template>
							</v-img>
						</v-col>
					</v-row>
				</v-container>
			</section>

			<section>
				<br><br><br><br>
				<v-row class="justify-center">
					<v-col cols="1" class="d-flex align-center justify-start">
						<v-btn tile color="#C4C4C4" height="55">
							<v-icon color="black" right>mdi-arrow-left</v-icon>
						</v-btn>
					</v-col>

					<v-col cols="10" class="d-flex align-center justify-center">
						<v-container fill-height>
							<v-card flat class="mx-auto" color="transparent">
								<div class="text-center my-10 py-10">
									<span class="text-uppercase font-bold" style="font-size: 60px; line-height: normal;">LoREM IPSUM
										<span class="text-uppercase font-bold" style="color: #D9EF0C;">LoREM</span>                
									</span>

									<v-row class="my-10">
										<v-img src="Ellipse.png" lazy-src="Ellipse.png" contain height="200">
											<template v-slot:placeholder>
											<v-row class="fill-height ma-0" align="center" justify="center">
												<v-progress-circular color="grey lighten-5"></v-progress-circular>
											</v-row>
											</template>
										</v-img>
									</v-row>

									<v-row align="center" justify="center">
										<v-col cols="12" sm="12" md="12" lg="12" xl="12">
											<span class="font-bold" style="font-size: 26px; line-height: 1.5em;">Lorem Ipsum is simply</span>
										</v-col>

										<v-col cols="12" sm="12" md="9" lg="9" xl="9">
											<span class="font-light" style="font-size: 18px">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</span>
										</v-col>
									</v-row>

							
								</div>
							</v-card>
						</v-container>
					</v-col>

					<v-col cols="1" class="d-flex align-center justify-end">
						<v-btn tile color="#D9EF0C" height="55">
							<v-icon color="black" right>mdi-arrow-right</v-icon>
						</v-btn>
					</v-col>
				</v-row>
				<br><br><br><br>
			</section>

			<section style="background-color: #D9EF0C">
				<v-container fill-height>
					<v-card flat class="mx-auto" color="transparent">
						<div class="text-center my-10 py-10">
							<span class="text-uppercase font-bold black--text" style="font-size: 60px; line-height: normal;">LoREM IPSUM</span>

							<v-row class="my-10" align="center" justify="center">
								<v-col 
									cols="12" sm="12" md="4" xl="4" lg="4" 
									v-for="product in products"
									:key="product.id"
								>	
									<v-card light class="text-left" height="550">
										<v-img
											:src="product.thumbnail"
											height="236px"
										></v-img>

										<v-card-text style="position: relative;">
											<v-btn
												absolute
												color="red"
												class="white--text font-medium"
												right
												fab
												top
											>
												-{{ Math.round(product.discountPercentage) }}%
											</v-btn>
										</v-card-text>

										<v-card-title class="font-bold">
											{{ product.title }}
										</v-card-title>

										<v-card-text class="font-light pb-0">
											
											<v-row align="center" class="mx-0">
												<v-rating
													:value="product.rating"
													color="amber"
													dense
													half-increments
													readonly
													size="14"
												></v-rating>
												<div class="grey--text ms-4">
													{{ product.rating }}
												</div>
											</v-row>
											<div class="my-4 font-light">
												{{ product.brand }}
											</div>
										</v-card-text>

										<v-card-subtitle style="height: 100px" class="pt-0 font-light black--text">
											{{ product.description }}
										</v-card-subtitle>

										<v-card-actions style="height: 50px; font-size: 30px" class="font-bold red--text">
											<v-spacer></v-spacer>
											฿{{ test(product.price) }}.-
										</v-card-actions>
									</v-card>
								</v-col>
							</v-row>					
						</div>
					</v-card>
				</v-container>
			</section>

			<section style="height: 1003px">
				<v-container fill-height>
					<v-card class="mx-auto" color="transparent">
						<v-row align="center" justify="center">
							<v-col cols="12" sm="12" md="6" lg="6" xl="6" align="center">
								<v-img src="Bicycle.png" lazy-src="Bicycle.png" contain height="423" width="719">
									<template v-slot:placeholder>
										<v-row class="fill-height ma-0" align="center" justify="center">
											<v-progress-circular color="grey lighten-5"></v-progress-circular>
										</v-row>
									</template>
								</v-img>
							</v-col>

							<v-col class="px-12" cols="12" sm="12" md="6" lg="6" xl="6" align="left">
								<v-card flat color="transparent">
									<v-card-title style="font-size: 60px" class="pl-0 ml-0 font-bold-thai">ติดต่อเรา</v-card-title>

									<div class="mt-6">
										<v-text-field
											label="ชื่อ-นามสกุล"
											class="font-light-thai"
											color="white"
										></v-text-field>

										<v-text-field
											label="เบอร์ติดต่อ"
											class="font-light-thai"
											color="white"
										></v-text-field>

										<v-text-field
											label="อีเมล"
											class="font-light-thai"
											color="white"
										></v-text-field>
										
										<v-menu
											ref="menu"
											v-model="menu"
											:close-on-content-click="false"
											transition="scale-transition"
											light
											offset-y
											max-width="290px"
											max-height="322px"
										>
											<template v-slot:activator="{ on, attrs }">
												<v-text-field
													:value="formatDate"
													label="วันที่"
													class="font-light-thai"
													color="white"
													append-icon="mdi-calendar-month-outline"
													readonly
													v-bind="attrs"
													v-on="on"
												></v-text-field>
											</template>
											<v-date-picker
												v-model="startDate"
												:weekday-format="getDay"
												color="#DEE34B"
												no-title
												scrollable
												@input="menu = false"
											></v-date-picker>
										</v-menu>
									</div>

									<div class="mt-5 font-light" style="font-size: 16px">
										Lorem Ipsum is simply dummy text <br>
										Lorem Ipsum is simply dummy te
									</div>

									<v-btn
										block
										rounded
										class="mt-13 font-medium black--text"
										style="background: linear-gradient(180deg, #DEE34B 0%, #D9EF0C 35.94%, #87A30D 100%);"
										height="56"
									>
										Lorem
									</v-btn>
								</v-card>
							</v-col>
						</v-row>
					</v-card>
				</v-container>
			</section>

		</v-main>
	</v-app>
</template>

<script>
import dayjs from 'dayjs'
const daysOfWeek = ['Sun', 'Mon', 'Tue', 'Wen', 'Thu', 'Fri', 'Sat'];

export default {
	layout: 'blank',
	data() {
		return {
			products: [],
			startDate: null,
      	menu: false,
		}
	},
	async asyncData({ $axios }) {
		let { data } = await $axios.get('https://dummyjson.com/products?limit=3')
		return { products : data.products }
	},
	computed: {
      formatDate() {
        	return this.startDate ? dayjs(this.startDate).format("DD/MM/YYYY") : dayjs().format("DD/MM/YYYY")
      },
	},
	methods: {
		getDay(date){
			let i = new Date(date).getDay(date)
			return daysOfWeek[i]
		},
		numberWithCommas(x) {
         return x.toString().replace(/\B(?<!\.\d*)(?=(\d{3})+(?!\d))/g, ",");
      },
      test(x) {
         const result = this.numberWithCommas(x);
         return result;
      },
	},
}
</script>

<style scoped>
	.v-text-field >>> label {
		color: white
	}
</style>

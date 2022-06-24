<template>
    <v-container fluid>
        <v-card class=" align-center justify-center" dark color="#FF7400" height="150" tile flat>
            <v-row>
                <v-col cols="12" sm="12">
                    <h3 class="text-center "> FAST FORWARD</h3>
                </v-col>
                <v-col cols="12" sm="12">
                    <v-breadcrumbs class="justify-center mt-n7" dark :items="items">
                        <template v-slot:divider>
                            <v-icon color="#008500">mdi-chevron-right</v-icon>
                        </template>
                    </v-breadcrumbs>
                </v-col>
            </v-row>
        </v-card>
        <v-card class="mx-16 mt-n10 card1" color="white" tile>
            <v-row>
                <v-col class="pr-0" cols="12" sm="8">
                    <v-card height="250px" tile flat color="#00A67C">
                        <v-row>
                            <v-col class="pl-8 pt-2" cols="12" sm="4">
                                <v-btn class="whithoutuppercase" small tile color="#150873" dark>new</v-btn>
                                <h6 class="white--text mt-8 text-uppercase">mountain bikes </h6>
                                <h3 class="white--text mt-5 text-uppercase">Orbea MX 40 </h3>
                                <v-btn class="whithoutuppercase px-8 mt-10" rounded color="#01A19C" dark>MORE INFO
                                </v-btn>
                            </v-col>
                            <v-col cols="12" sm="8">
                                <v-img class="mt-n2" src="../assets/image/bike-1.png" max-width="400" max-height="400"
                                    contain></v-img>
                            </v-col>
                        </v-row>
                    </v-card>
                </v-col>
                <v-col class="pl-0 " cols="12" sm="4">
                    <v-card height="250px" tile flat color="#01A19C">
                        <v-row>
                            <v-col class="pl-8 pt-2" cols="12" sm="6">
                                <v-btn class="whithoutuppercase" color="#150873" dark small>new</v-btn>
                                <h6 class="white--text mt-8 text-uppercase">Shop latest collection </h6>
                                <h3 class="white--text mt-5 text-uppercase ">Sale and clearance</h3>
                                <v-btn class="whithoutuppercase px-8 mt-5" rounded color="#02b38C" dark> Shop now
                                </v-btn>
                            </v-col>
                            <v-col cols="12" sm="6">
                                <v-img class="mt-2" src="../assets/image/kurt-1.png" max-width="400" max-height="420"
                                    contain></v-img>
                            </v-col>
                        </v-row>
                    </v-card>
                </v-col>
            </v-row>
            <v-row>
                <v-col class="mt-n6 pr-0" cols="12" sm="3">
                    <v-toolbar flat outlined>
                        <v-toolbar-title><strong>Filter</strong></v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-divider vertical></v-divider>
                        <v-btn class="ml-1" icon>
                            <v-icon color="#02b38C">
                                mdi-sync
                            </v-icon>
                        </v-btn>
                    </v-toolbar>
                </v-col>
                <v-col class="mt-n6 px-0" cols="12" sm="3">
                    <v-toolbar flat outlined>
                        <v-toolbar-title>
                            CITY BY: <span>Price: $-$$</span>
                        </v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-btn class="mr-4" icon>
                            <v-icon color="#150873">
                                mdi-menu-down
                            </v-icon>
                        </v-btn>
                    </v-toolbar>
                </v-col>
                <v-col class="mt-n6 px-0" cols="12" sm="3">
                    <v-toolbar class="" flat outlined>
                        <v-toolbar-title>SHOW: <span>15</span></v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-btn class="mr-4" icon>
                            <v-icon color="#150873">
                                mdi-menu-down
                            </v-icon>
                        </v-btn>
                    </v-toolbar>
                </v-col>
                <v-col class="mt-n6 pl-0" cols="12" sm="3">
                    <v-toolbar flat outlined>
                        <v-btn class="mr-1" icon>
                            <v-icon color="#02b38C">mdi-apps</v-icon>
                        </v-btn>
                        <v-divider vertical></v-divider>
                        <v-btn class="mx-1" icon>
                            <v-icon color="#FF7400">mdi-format-list-bulleted</v-icon>
                        </v-btn>
                        <v-divider vertical></v-divider>
                        <v-toolbar-title class="ml-2">
                            <strong>COMPARE :</strong>
                        </v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-badge class="mr-2" color="#FF7400" content="3"></v-badge>
                    </v-toolbar>
                </v-col>
                <v-col class="py-0 pr-0 mt-3 " cols="3">
                    <v-card flat outlined tile>
                        <v-toolbar flat>
                            <v-icon class="mr-2" color="#150873">mdi-chevron-down</v-icon>
                            <strong class="text-uppercase">Category </strong>
                            <v-spacer></v-spacer>
                            <v-icon color="#02b38C" small>mdi-close</v-icon>
                        </v-toolbar>
                        <v-list class="mt-n5" dense>
                            <v-list-item v-for="product in products" :key="product.title">
                                <v-list-item-content>
                                    <v-list-item-title class="ml-8" v-text="product.title"></v-list-item-title>
                                </v-list-item-content>
                                <v-list-item-action>
                                    <v-list-item-subtitle v-text="product.count"></v-list-item-subtitle>
                                </v-list-item-action>
                            </v-list-item>
                        </v-list>
                    </v-card>
                    <v-card flat outlined tile>
                        <v-toolbar flat>
                            <v-icon class="mr-2" color="#150873">mdi-chevron-down</v-icon>
                            <strong>PRICE</strong>
                            <v-spacer></v-spacer>
                            <v-icon color="#02b38C" small>mdi-close</v-icon>
                        </v-toolbar>
                        <v-toolbar flat>
                            <v-text-field class="mx-2" placeholder="$100" filld rounded dense></v-text-field>
                            <v-text-field class="mx-2" placeholder="$4999.99" filld rounded dense></v-text-field>
                        </v-toolbar>
                        <v-range-slider color="#150873" max="50" min="-40"></v-range-slider>
                    </v-card>
                    <v-card flat outlined tile>
                        <v-toolbar flat>
                            <v-icon class="mr-2" color="#150873">mdi-chevron-down</v-icon>
                            <strong class=" text-uppercase">BRAKE TYPE</strong>
                            <v-spacer></v-spacer>
                            <v-icon color="#02b38C" small>mdi-close</v-icon>
                        </v-toolbar>
                        <v-list class="mt-n5" dense>
                            <v-list-item v-for="btype in btypes" :key="btype.title">
                                <v-list-item-content>
                                    <v-list-item-title class="ml-6" v-text="btype.title"></v-list-item-title>
                                </v-list-item-content>
                                <v-list-item-action>
                                    <v-checkbox color="primary" v-model="btype.sta"></v-checkbox>
                                </v-list-item-action>
                            </v-list-item>
                        </v-list>
                    </v-card>
                    <v-card flat outlined tile>
                        <v-toolbar flat>
                            <v-icon class="mr-2" color="#150873">mdi-chevron-down</v-icon>
                            <strong class=" text-uppercase">Wheel diameter</strong>
                            <v-spacer></v-spacer>
                            <v-icon color="#02b38C" small>mdi-close</v-icon>
                        </v-toolbar>
                        <v-chip-group class="ml-2" column multiple active-class="orange white--text">
                            <v-chip class="size" v-for="size in sized" :key="size" :value="size">
                                {{ size }}
                            </v-chip>
                        </v-chip-group>
                    </v-card>
                </v-col>
                <v-col class="mt-n3" cols="9">
                    <v-row>
                        <v-col cols="12" sm="4" v-for="(bike, i) in biked" :key="i" :class="bike.class">
                            <v-hover v-slot:default="{ hover }">
                                <v-card height="300" align="center" flat outlined tile>
                                    <v-card-actions>
                                        <v-spacer></v-spacer>
                                        <v-btn color="#150873" small dark>{{ bike.solid }}</v-btn>
                                    </v-card-actions>
                                    <v-img :src=bike.image width="200" height="200" contain></v-img>
                                    <v-card-text class="mt-n4">
                                        <strong :class="hover ? 'orange--text dark' : 'black--text'">{{ bike.title
                                        }}</strong>
                                    </v-card-text>
                                    <v-expand-transition>
                                        <div v-if="hover"
                                            class="d-flex transition-fast-in-fast-out orange v-card--reveal display-3 white--text"
                                            style="height: 100%; ">
                                            <v-btn rounded color="white">
                                                <v-icon>mdi-cart-outlined</v-icon>
                                                Buy
                                            </v-btn>
                                            <v-btn class="ml-2" fab small color="white">
                                                <v-icon color="#02b38C">mdi-content-copy</v-icon>
                                            </v-btn>
                                            <v-btn class="ml-2" fab small color="white">
                                                <v-icon color="#02b38C">mdi-heart-outline</v-icon>
                                            </v-btn>

                                        </div>
                                    </v-expand-transition>
                                </v-card>
                            </v-hover>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col class="mt-n3 pr-0 pb-0" cols="12" sm="3">
                    <v-toolbar flat outlined>

                    </v-toolbar>
                </v-col>
                <v-col class="mt-n3 px-0 pb-0" cols="12" sm="3">
                    <v-toolbar flat outlined>
                        <v-btn class="mr-1" icon>
                            <v-icon color="#150873">mdi-chevron-up</v-icon>
                        </v-btn>
                        <v-divider vertical></v-divider>
                    </v-toolbar>
                </v-col>
                <v-col class="mt-n3 px-0 pb-0" cols="12" sm="3" >
                    <v-toolbar class="text-center" flat outlined >
                        <v-pagination :length="4" v-model="page"></v-pagination>
                    </v-toolbar>
                </v-col>
                <v-col class="mt-n3 pl-0 pb-0" cols="12" sm="3">
                    <v-toolbar flat outlined>
                        <v-btn class="mr-1" icon>
                            <v-icon color="#150873">mdi-chevron-down</v-icon>
                        </v-btn>
                        <v-divider vertical></v-divider>
                    </v-toolbar>
                </v-col>
            </v-row>
        </v-card>
        
    </v-container>
</template>

<script>
export default {
    data: () => ({
        page:1,
        items: [
            {
                text: 'Home',
                disabled: false,
                href: 'breadcrumbs_home',
            },
            {
                text: 'Catalog',
                disabled: false,
                href: 'breadcrumbs_catalog',
            },
            {
                text: 'Road',
                disabled: false,
                href: 'breadcrumbs_road',
            },
            {
                text: 'Kids',
                disabled: false,
                href: 'breadcrumbs_kids',
            },

        ],
        products: [
            {
                title: 'Mens`s bikes',
                count: '25',
            },
            {
                title: 'Women`s bikes',
                count: '5',
            },
            {
                title: 'Mountaine bikes',
                count: '52',
            },
            {
                title: 'Road bikes',
                count: '8',
            },
            {
                title: 'Hybrid bikes',
                count: '14',
            },
            {
                title: 'Electric bikes',
                count: '10',
            },
        ],
        btypes: [
            {
                title: 'Hydraulic disc',
                sta: true,
            },
            {
                title: 'Mechanical disc',
                sta: false,
            },
            {
                title: 'Linear pull',
                sta: true,
            },
            {
                title: 'Coaster',
                sta: true,
            },
            {
                title: 'Caliper',
                sta: false,
            },
        ],
        sized: [
            '9"', '12"', '14"', '16"', '18"', '20"', '20"+', '22"', '24"', '24"+',
        ],
        biked: [
            {
                class: 'pa-0',
                solid: '-10%',
                image: 'cart-1.png',
                title: 'Orbea MX 50',
                price: '$ 2000.00',
            },
            {
                class: 'pa-0',
                solid: '-30%',
                image: 'cart-1.png',
                title: 'Cannondale Trail SE 4',
                price: '$ 209.08',
            },
            {
                class: 'pa-0',
                solid: '-1%',
                image: 'cart-1.png',
                title: ' MaxxPro M300',
                price: '$ 6987.00',
            },
            {
                class: 'pa-0',
                solid: '-32%',
                image: 'cart-1.png',
                title: 'Cyclone AX 29',
                price: '$ 800.33',
            },
            {
                class: 'pa-0',
                solid: '-10%',
                image: 'cart-1.png',
                title: 'Reid Rapid Drop Bar',
                price: '$ 2540.00',
            },
            {
                class: 'py-0 pl-0',
                solid: '-40%',
                image: 'cart-1.png',
                title: 'VNC RockRider A5 29',
                price: '$ 19800.00',
            },
            {
                class: 'pa-0',
                solid: '-80%',
                image: 'cart-1.png',
                title: 'Spirit Echo 7.2',
                price: '$ 5400.00',
            },
            {
                class: 'pa-0',
                solid: '-70%',
                image: 'cart-1.png',
                title: 'Reid MTB Pro Disc',
                price: '$ 2000.00',
            },
            {
                class: 'pa-0',
                solid: '-22%',
                image: 'cart-1.png',
                title: 'Winner Solid DX',
                price: '$ 6020.00',
            },
            {
                class: 'pa-0',
                solid: '-10%',
                image: 'cart-1.png',
                title: 'Polygon Heist X2',
                price: '$ 2500.00',
            },
        ],

    })
}
</script>

<style>
.container {
    padding: 0;
}

.v-btn.whithoutupercase {
    text-decoration: none;
}

.v-chip.v-size--def {
    border-radius: 50px;
    font-size: 14px;
    height: 40px;
    width: 40px;
}

.v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .5;
    position: absolute;
    width: 100%;
}

.card-first {
    z-index: 10;
}

.card-second {
    z-index: 1;
}
</style>
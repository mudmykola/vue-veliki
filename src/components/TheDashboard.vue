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
                    </v-toolbar>
                </v-col>
            </v-row>
        </v-card>
    </v-container>
</template>

<script>
export default {
    data: () => ({
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
    widows: 100%;
}

.card-first {
    z-index: 10;
}

.card-second {
    z-index: 1;
}
</style>
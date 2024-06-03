<!-- https://github.com/zakaria-29-dev/Create-A-Tour-Travel-Agency-Website-Design-Using-Vuejs-and-Vuetify-HTML-CSS-JAVASCRIPT-/tree/main -->
<template>
  <Navbar />
  <v-main>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-row>
            <v-col cols="12" sm="6">
              <h1 class="title1">
                It's A Big World<br/>
                Our There, Go <br/>Explore
              </h1>
              <p class="part1">
                It has survived not only five centuries,<br/>
                but also the leap into electronic typesetting,<br/> 
                remaining essentially unchanged.
              </p>
              <v-btn class="text-none mt-8 bt1" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0">
                Get Exploration
              </v-btn>
              <v-btn class="text-none text-indigo-lighten-1 mt-8" size="x-large" variant="flat" rounded="0">
                Read More
              </v-btn>
            </v-col>
            <v-col cols="12" sm="6">
              <v-img src="/3.jpg" class="img1"></v-img>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat>
            <v-tabs v-model="tab" color="indigo-lighten-1" align-tabs="center">
              <v-tab :value="1">
                <v-icon class="mr-2">mdi mdi-bed</v-icon>Hotel
              </v-tab>
              <v-tab :value="2">
                <v-icon class="mr-2">mdi mdi-airplane-takeoff</v-icon>Flight
              </v-tab>
              <v-tab :value="3">
                <v-icon class="mr-2">mdi mdi-car</v-icon>Car
              </v-tab>
              <v-tab :value="4">
                <v-icon class="mr-2">mdi mdi-ferry</v-icon>Ship
              </v-tab>
            </v-tabs>
            <v-window v-mode="tab">
              <v-window-item v-for="n in 4" :key="n" :value="n">
                <v-container fluid>
                  <v-row>
                    <v-col cols="12" sm="2">
                      <div class="text-subtitle-1 text-medium-emphasis">Your Destination</div>
                      <v-select density="compact" placeholder="Destination" :items="[
                        'California',
                        'Colorado',
                        'Florida',
                        'Georgia',
                        'Texas',
                        'Wyoming'
                      ]" variant="outlined">
                      </v-select>
                    </v-col>
                    <v-col cols="12" sm="2">
                      <div class="text-subtitle-1 text-medium-emphasis">Check in</div>
                      <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
                    </v-col>
                    <v-col cols="12" sm="2">
                      <div class="text-subtitle-1 text-medium-emphasis">Check out</div>
                      <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
                    </v-col>
                    <v-col cols="12" sm="2">
                      <div class="text-subtitle-1 text-medium-emphasis">Child</div>
                      <v-select density="compact" placeholder="Child" :items="[
                        '1',
                        '2',
                        '3',
                        '4',
                        '5',
                        '6'
                      ]" variant="outlined">
                      </v-select>
                    </v-col>
                    <v-col cols="12" sm="2">
                      <div class="text-subtitle-1 text-medium-emphasis">Adult</div>
                      <v-select density="compact" placeholder="Adult" :items="[
                        '1',
                        '2',
                        '3',
                        '4',
                        '5',
                        '6'
                      ]" variant="outlined">
                      </v-select>
                    </v-col>
                    <v-col cols="12" sm="2">
                      <v-btn class="text-none mt-5" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                        Book now
                      </v-btn>
                    </v-col>
                  </v-row>
                </v-container>
              </v-window-item>
            </v-window>
          </v-card>
        </v-col>
        <v-col cols="12" sm="12">
          <h4 class="text-center text-indigo-lighten-1">Featured Tours</h4>
          <h1 class="text-center">Beautiful Places Arround The World</h1>
          <v-row justify="center">
            <v-col cols="12" sm="10">
              <v-row>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-hover v-slots="{ isHovering, props }">
                    <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props" class="card1">
                      <v-img src="/5.jpg" cover height="100%">
                        <div class="d-flex flex-row-reverse">
                          <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                            3 Packages
                          </v-btn>
                        </div>
                      </v-img>
                    </v-card>
                  </v-hover>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
  <Footer />
</template>

<script setup>
  //
</script>
<script>
export default {
  data: () => ({
    tab: null,
    model: null,
    icons: ["mdi-rewind", "mdi-play", "mdi-fast-forward"],
    transparent: "rgba(255, 255, 255, 0)",
    rating: 4.5,
    populars: [
      {
        image: "9.jpg",
        title: " Enjoy The Beauty Place in Greece City",
        subtitle1: "Greece",
        subtitle2: "4 Day's 3 Night",
        money: "$1200",
      },
      {
        image: "10.jpg",
        title: " Enjoy The Beauty Place in Maldivs Beach",
        subtitle1: "Maldivs",
        subtitle2: "5 Day's 4 Night",
        money: "$1300",
      },
      {
        image: "11.jpg",
        title: " Enjoy The Beauty Place in Bhutan City",
        subtitle1: "Bhutan",
        subtitle2: "3 Day's 2 Night",
        money: "$900",
      },
      {
        image: "12.jpg",
        title: " Enjoy The Beauty Place in Paris City",
        subtitle1: "Paris",
        subtitle2: "4 Day's 3 Night",
        money: "$1700",
      },
    ],
    offers: [
      {
        image: "i1.png",
        title: " Different Coutries",
      },
      {
        image: "i2.png",
        title: " Bus Tours",
      },
      {
        image: "i3.png",
        title: " Food Tours",
      },
      {
        image: "i4.png",
        title: " Summer Rest",
      },
      {
        image: "i5.png",
        title: "Ship Cruises",
      },
      {
        image: "i6.png",
        title: "Mountains Tours",
      },
    ],
    hotels: [
      {
        image: "h1.jpg",
        title: " Enjoy The Beauty Place in Greece City",
        subtitle1: "Greece",
        subtitle2: "4 Day's 3 Night",
        money: "$1200",
      },
      {
        image: "h2.jpg",
        title: " Enjoy The Beauty Place in Maldivs Beach",
        subtitle1: "Maldivs",
        subtitle2: "5 Day's 4 Night",
        money: "$1300",
      },
      {
        image: "h3.jpg",
        title: " Enjoy The Beauty Place in Bhutan City",
        subtitle1: "Bhutan",
        subtitle2: "3 Day's 2 Night",
        money: "$900",
      },
      {
        image: "h4.jpg",
        title: " Enjoy The Beauty Place in Paris City",
        subtitle1: "Paris",
        subtitle2: "4 Day's 3 Night",
        money: "$1700",
      },
    ],
    travels: [
      {
        image: "f1.jpg",
      },
      {
        image: "f2.jpg",
      },
      {
        image: "f3.jpg",
      },
      {
        image: "f4.jpg",
      },
      {
        image: "f5.jpg",
      },
      {
        image: "f6.jpg",
      },
      {
        image: "5.jpg",
      },
      {
        image: "8.jpg",
      },
    ],
  }),
};
</script>
<style scoped>
  .title1 {
    color: #1f3347;
    font-size: 50px;
    font-style: bold;
    margin-left: 100px;
    margin-top: 70px;
  }
  .part1 {
    color: "AAA1B4";
    margin-left: 100px;
  }
  .bt1 {
    margin-left: 100px;
  }
  .img1 {
    width: 1000px !important;
    height: 1000px !important;
    z-index: 1;
    margin-top: -200px;
  }
  .v-card.card1 {
    transition: opacity 0.4s ease-in-out;
  }
  .v-card.card1:not(.on-hover) {
    opacity: 0.6;
  }
  .show-btns {
    color: rgba(255, 255, 255, 1) !important;
  }
  .top {
  margin-top: 100%;
  margin-left: 20px;
}
.v-card--reveal {
  align-items: end;
  bottom: 0;
  justify-content: start;
  opacity: 0.9;
  position: absolute;
  width: 100%;
}
.ligne1 {
  margin-top: 150px;
}
.ligne2 {
  margin-top: 10px;
  padding: 0 250px 0 250px;
}
.tp {
  margin-top: -2px;
}
</style>
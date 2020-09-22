<template>
<div>
    <carousel />
    <v-divider class="py-2 success"></v-divider>
    <v-col class="lighten-2 py-6 text-center " cols="12">
      <v-hover v-slot:default="{ hover }" open-delay="200">
      <v-card :loading="loading" :elevation="hover ? 16 : 2" class="pa-md-4 mx-lg-auto" color="white">
        <v-card-text>
          <v-spacer></v-spacer>
            <h1 style="color:#800040;">Media Health</h1>
          <v-spacer></v-spacer>
          <p class="py-5" style="text-align:justify">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure consequuntur dolor eligendi hic voluptatum modi natus quam ea rerum architecto. Non porro earum perferendis enim magnam tempore eos minima reprehenderit!
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam accusamus aperiam sint molestiae architecto quidem eos optio laborum amet nihil, voluptatum, culpa voluptatibus in, delectus ab doloribus quasi nemo recusandae.
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Adipisci eveniet autem atque et quisquam veniam, rem repellat, nisi ea exercitationem cum deleniti laborum perspiciatis quos qui? Cumque placeat delectus unde.
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure consequuntur dolor eligendi hic voluptatum modi natus quam ea rerum architecto. Non porro earum perferendis enim magnam tempore eos minima reprehenderit!
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam accusamus aperiam sint molestiae architecto quidem eos optio laborum amet nihil, voluptatum, culpa voluptatibus in, delectus ab doloribus quasi nemo recusandae.
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Adipisci eveniet autem atque et quisquam veniam, rem repellat, nisi ea exercitationem cum deleniti laborum perspiciatis quos qui? Cumque placeat delectus unde.
          </p>
        </v-card-text>
      </v-card>
      </v-hover>
    </v-col>
    <v-divider class="py-2 primary"></v-divider>

    <v-row>
       <v-col class="py-4 text-center" cols="12">
          <v-spacer></v-spacer>
             <h1 style="color:#800040;">Our Services</h1>
          <v-spacer></v-spacer>
       </v-col>
      <v-col cols="12" sm="4" v-for="n in 6" :key="n"  style="margin-top:-40px">
        <v-hover v-slot:default="{ hover }" open-delay="200">
          <v-card :loading="loading" :elevation="hover ? 16 : 2" class="pa-2 my-12" height="600px" max-width="410" tile outlined>
            <v-img  height="250" src="https://cdn.vuetifyjs.com/images/cards/cooking.png" ></v-img>
            <v-card-title>Cafe Badilico</v-card-title>
            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="4.5"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>
                <div class="grey--text ml-4">4.5 (413)</div>
              </v-row>
              <div class="my-4 subtitle-1">
                $ • Italian, Cafe
              </div>
              <div>
                Small plates, salads & sandwiches - an intimate setting with 12
                indoor seats plus patio seating.
              </div>
            </v-card-text>
            <v-divider class="mx-4"></v-divider>
            <v-card-title>Tonight's availability</v-card-title>
            <v-card-text>
              <v-chip-group
                v-model="selection"
                active-class="deep-purple accent-4 white--text"
                column
              >
                <v-chip>5:30PM</v-chip>
                <v-chip>7:30PM</v-chip>
                <v-chip>8:00PM</v-chip>
                <v-chip>9:00PM</v-chip>
              </v-chip-group>
            </v-card-text>
            <v-card-actions>
              <v-btn color="deep-purple lighten-2" text @click="reserve">
                Reserve
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
    <v-divider class="py-2 primary"></v-divider>
    <v-col class="lighten-2 py-8 text-center " cols="12">
      <v-spacer></v-spacer>
      <h3 style="color:#800040;">Our Clients</h3>
      <v-spacer></v-spacer>
    </v-col>
    <v-row class="py-2">
      <v-col v-for="n in 4" :key="n">
        <v-card class="pa-2" tile outlined>
          <v-card class="mx-auto" max-width="250">
            <v-img
              src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
              height="100px"
            ></v-img>

            <v-card-title>
              Top western road trips
            </v-card-title>

            <v-card-subtitle>
              1,000 miles of wonder
            </v-card-subtitle>

            <v-card-actions>
              <v-btn text>Share</v-btn>

              <v-btn color="purple" text>
                Explore
              </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? "mdi-chevron-up" : "mdi-chevron-down"
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  I'm a thing. But, like most politicians, he promised more than
                  he could deliver. You won't have time for sleeping, soldier,
                  not with all the bed making you'll be doing. Then we'll go
                  with that data file! Hey, you add a one and two zeros to that
                  or we walk! You're going to do his laundry? I've got to find a
                  way to escape.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-card>
      </v-col>
    </v-row>
    <v-divider class="py-2 primary"></v-divider>
</div>
</template>

<script>
// @ is an alias to /src
import carousel from "@/components/carousel.vue";

export default {
  name: "Home",
  components: {
    carousel
  },
};
</script>
<style lang="scss">

</style>

<template>
<div>
  <v-col class="lighten-2 py-6 text-center " cols="12">
      <v-hover v-slot:default="{ hover }" open-delay="200">
      <v-card :loading="loading" :elevation="hover ? 16 : 2" class="pa-md-4 mx-lg-auto" color="white">
        <v-card-text>
          <v-spacer></v-spacer>
            <h1 style="color:#800040;">Contact Us</h1>
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
  


</div>
</template>
<script>
  export default {
    data: () => ({
      menu: false,
    }),
  }
</script>

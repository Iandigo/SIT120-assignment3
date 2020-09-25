<template>
<!-- Picture Gallery -->
  <div class="block galleryBlock">
    <v-container>
      <v-text-field
            v-model="search"
            placeholder="Search"
            prepend-inner-icon="mdi-magnify"
            class="expanding-search"
            filled
            dense
          ></v-text-field>

      <h2 class="text-center">Pictures</h2>
      <v-row>
        <v-col v-for="item in filterItems" :key="item.id" class="d-flex child-flex" cols="6" sm="4">
          <v-hover>
            <template v-slot:default="{ hover }">
              <v-card flat tile class="d-flex">
                <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2">
                  <template v-slot:placeholder>
                    <v-row class="fill-height ma-0" align="center" justify="center">
                      <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
                <v-fade-transition>
                  <v-overlay
                    v-if="hover"
                    absolute
                    color="#036358"
                  >
                    <h1>{{item.title}}</h1>
                  </v-overlay>
                </v-fade-transition>
              </v-card>
            </template>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "picture",

  data() {
    return {
      search:'',

      items: [
        {
          id: 1,
          src: require("../assets/images/img1.jpg"),
          title: 'Study corner'
        },
        {
          id: 2,
          src: require("../assets/images/img2.jpg"),
          title: 'Winter'
        },
        {
          id: 3,
          src: require("../assets/images/img3.jpg"),
          title: 'Camera'
        },
        {
          id: 4,
          src: require("../assets/images/img4.jpg"),
          title: 'Train'
        },
        {
          id: 5,
          src: require("../assets/images/img5.jpg"),
          title: 'Bird'
        },
        {
          id: 6,
          src: require("../assets/images/img6.jpg"),
          title: 'Deer'
        },
        {
          id: 7,
          src: require("../assets/images/img7.jpg"),
          title: 'Shoes'
        },
        {
          id: 8,
          src: require("../assets/images/img8.jpg"),
          title: 'Elevator'
        },
        {
          id: 9,
          src: require("../assets/images/img9.jpg"),
          title: 'Sports'
        }
      ],
    };
  },
  
  computed: {
    filterItems: function(){
      return this.items.filter((item) => {
        return item.title.toLowerCase().match(this.search)
      });
    }
  },
};
</script>
<template>
  <v-app>
  <v-card
    class="overflow-hidden" style="height: 100vh"
  >
    <v-system-bar style="background: #161d30"></v-system-bar>

    <v-app-bar
      style="background: #161d30"
      dark
      prominent
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Avaliação Sub</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-filter</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <v-avatar color="red">
        <span class="white--text text-h6">FM</span>
      </v-avatar>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      style="background: #242b3e"
      absolute
      left
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-view-dashboard</v-icon></v-btn>
            <v-list-item-title class="text-white">Dashboard</v-list-item-title>
          </v-list-item>
          <v-spacer class="py-3"></v-spacer>
          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-email</v-icon></v-btn>
            <v-list-item-title class="text-white">Email</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-message</v-icon></v-btn>
            <v-list-item-title class="text-white">Chat</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-magnify</v-icon></v-btn>
            <v-list-item-title class="text-white">Todo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-calendar</v-icon></v-btn>
            <v-list-item-title class="text-white">Calendar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-receipt</v-icon></v-btn>
            <v-list-item-title class="text-white">Invoice</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-cart</v-icon></v-btn>
            <v-list-item-title class="text-white">eCommerce</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-btn icon><v-icon class="text-white">mdi-account</v-icon></v-btn>
            <v-list-item-title class="text-white">User</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-card-text id="content">
    <div>
      <v-container
      v-for="align in 1"
      :key="align"
      class="grey lighten-5 mb-6"
    >
      <v-row
        :align="align"
        style="height: 150px;"
        class="mt-5"
      >
        <v-col
          v-for="n in 2"
          :key="n"
        >
          <v-card
    class="mx-auto"
    color="#26c6da"
    dark
    max-width="400"
  >
    <v-card-title>
      <v-icon
        large
        left
      >
        mdi-twitter
      </v-icon>
      <span class="text-h6 font-weight-light">Twitter</span>
    </v-card-title>

    <v-card-text class="text-h5 font-weight-bold">
      "Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid as well."
    </v-card-text>

    <v-card-actions>
      <v-list-item class="grow">
        <v-list-item-avatar color="grey darken-3">
          <v-img
            class="elevation-6"
            alt=""
            src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
          ></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Evan You</v-list-item-title>
        </v-list-item-content>

        <v-row
          align="center"
          justify="end"
        >
          <v-icon class="mr-1">
            mdi-heart
          </v-icon>
          <span class="subheading mr-2">256</span>
          <span class="mr-1">·</span>
          <v-icon class="mr-1">
            mdi-share-variant
          </v-icon>
          <span class="subheading">45</span>
        </v-row>
      </v-list-item>
    </v-card-actions>
  </v-card>
        </v-col>
      </v-row>
    </v-container>
    </div>
    </v-card-text>
  </v-card>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {
  },

  data: () => ({
    drawer: false,
    group: null,

    alignments: [
        'start',
        'center',
        'end',
      ],
  }),

  watch: {
      group () {
        this.drawer = false
      },
    },
};
</script>

<style>
</style>

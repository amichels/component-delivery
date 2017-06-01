<template>
  <div>
    <v-navigation-drawer
      persistent
      v-model="drawer"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-tile value="true">
            <v-list-tile-action>
              <v-icon light v-html="item.icon"></v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title v-text="item.title"></v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar>
      <v-toolbar-side-icon @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
  </div>
</template>

<script>

  export default {
    data () {
      return {
        drawer: true,
        items: [
          { icon: 'shopping_cart', title: 'Order Lite' },
          { icon: 'attach_money', title: 'Pricing' },
          { icon: 'stars', title: 'Promotions' },
          { icon: 'group', title: 'Groups' },
          { icon: 'settings', title: 'Preferences' }
        ],
        title: 'E-commerce Administration'
      }
    }
  }
</script>
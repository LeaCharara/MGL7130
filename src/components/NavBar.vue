<template>
    <v-navigation-drawer clipped
    app
    permanent>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="item.link"
        >
          <!-- <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon> -->

          <v-list-item-content>
            <v-img style="height: 50px" src="https://picsum.photos/id/11/500/300"></v-img>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    data () {
      return {
        items: [
          { title: 'Dashboard', icon: 'mdi-cloud-search', link:'' },
          { title: 'Photos', icon: 'mdi-image', link:'' },
          { title: 'About', icon: 'mdi-help-box', link:'' },
        ],
        right: null,
      }
    },
}
</script>

<style>

</style>
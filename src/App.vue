<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title>
           <h2>Cần Thơ vivu</h2>
          </v-list-item-title>
          <!-- <v-list-subtitle>
          Du lịch đó đây
          </v-list-subtitle> -->
          <v-img src=""></v-img>
        </v-list-item-content>
      </v-list-item>
      <v-list dense>
      <v-list-item-group color="primary">
        <v-list-item style="color: green" v-for="(item, i) in items" :key="i" :to="item.link" link>
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title style="font-size: 16px" v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    </v-navigation-drawer>
    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Những địa điểm du lịch Cần Thơ HẤP DẪN nhất</v-toolbar-title>
    </v-app-bar>
    <v-main>
      <!--  -->
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>

  export default {
    data: () => ({ 
      drawer: null,
      items: [
        { title: 'Trang chủ', icon: 'mdi-home', link:"/" },
        { title: 'Thêm bài viết', icon: 'mdi-note-plus', link:"/add-post" },
        
      ],
    }),
    
  }
</script>
<template>
  <div>
  <v-app>



      <v-navigation-drawer
    
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
            subtitle="DIT-3B"
            title="Mark Joseph Escobal"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-folder" title="Dashboard" value="myfiles"></v-list-item>
          <v-list-item to="/category" prepend-icon="mdi-account-multiple" title="Category" value="shared"></v-list-item>
          <v-list-item to="/inventory" prepend-icon="mdi-star" title="Inventory" value="starred"></v-list-item>
          <v-list-item to="/users" prepend-icon="mdi-star" title="User" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>
    <v-app-bar>
  <template v-slot:prepend>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar> 
    <v-main>
      <v-container>
        <slot />
      </v-container>
    </v-main>
  </v-app>

  </div>







  
</template>

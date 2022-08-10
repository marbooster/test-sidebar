<template>
  <div id="app">
    <SideBarApp :menus="menus" :showmenu="showmenu" :isOpen="isOpen" :showSide="showSide" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import SideBarApp from "mairie-sidebar-app";

export default Vue.extend({
  name: 'App',
  components: {
    SideBarApp
  },
   data() {
    return {
      menus: [
        {
          link: "/settingsOrchestre",
          titleMenu: "SettingsOrchestre",
          menuIcon: "face",
        },
        {
          link: "/featuresOrchestre",
          titleMenu: "Features",
          menuIcon: "streetview",
          subMenus: [
            {
              title: "PagesOrchestre",
              link: "/pagesOrchestre",
              icon: "streetview",
            },
            {
              title: "ElementsOrchestre",
              link: "/elementsOrchestre",
              icon: "streetview",
            },
          ],
        },
        {
          link: "/ServicesOrchestre",
          titleMenu: "Services",
          menuIcon: "face",
          subMenus: [
            {
              title: "App Design Orchestre",
              link: "/app-designOrchestre",
              icon: "account_circle",
            },
            {
              title: "Web Design Orchestre",
              link: "/web-designOrchestre",
              icon: "work",
            },
          ],
        },
        {
          link: "/OverviewOrchestre",
          titleMenu: "OverviewOrchestre",
          menuIcon: "settings",
        }
      ],
      showmenu: false,
      isOpen: false,
      showSide: true, 
    }
  },
});
</script>
<style lang="scss">
@import "app.scss";
</style>
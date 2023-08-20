import { createApp } from 'vue'
import App from './App.vue'
import vueAwesomeSidebar from 'vue-awesome-sidebar'
import 'vue-awesome-sidebar/dist/vue-awesome-sidebar.css'
const app = createApp(App)
app.use(vueAwesomeSidebar)
app.mount("#app")
// OR Locally
import vueAwesomeSidebar from 'vue-awesome-sidebar'
import 'vue-awesome-sidebar/dist/vue-awesome-sidebar.css'
export default {
  components: {
    vueAwesomeSidebar
  }
}
2. Create a basic sidebar navigation on your web app.

<template>
  <VueAwesomeSideBar
    v-model:miniMenu="miniMenu"
    v-model:collapsed="collapsed"
    :menu="myMenu"
    vueRouterEnabel
  ></VueAwesomeSideBar>
</template>
<script setup>
import { ref } from 'vue'
const collapsed = ref(false)
const miniMenu = ref(false)
const myMenu = [
  {
    name: 'Getting Started',
    icon: { text: 'home' , class: 'material-icons-outlined' },
    children: [
      {
        name: 'level 1.1',
        href: '/a',
        icon: { text: 'home' , class: 'material-icons-outlined'},
        children: [
          {
            href: '/b',
            name: 'level 1.1.1',
          },
        ]
      },
      {
        name: 'level 1.2'
      }
    ],
  },
  {
    header: 'Settings'
  },
  {
    name: 'Dashboard',
    icon: { class: 'material-icons-outlined', text: 'dashboard' },
    children: [
      {
        href: '/c',
        name: 'level 2.1',
      },
    ]
  },
  {
    name: 'close menu',
    icon: { text: 'settings', class: 'material-icons-outlined' },
  },
]
</script>
3. Available sidebar props.

menu: {
  type: Array,
  required: true
},
menuType: {
  type: String,
  default: 'simple' // OR "fully"
},
collapsed: {
  type: Boolean,
  default: false
},
miniMenu: {
  type: Boolean,
  default: false
},
animationDuration: {
  type: Number,
  default: 300
},
width: {
  type: String,
  default: '290px'
},
widthMiniMenu: {
  type: String,
  default: '65px'
},
autoCollapse: {
  type: Number,
  default: null
},
removeIconSpace: {
  type: Boolean,
  default: false
},
closeOnClickOutSide: {
  type: Boolean,
  default: false
},
overLayerOnOpen: {
  type: Boolean,
  default: false
},
childrenOpenAnimation: {
  type: Boolean,
  default: true
},
position: {
  type: String,
  default: 'fixed'
},
keepChildrenOpen: {
  type: Boolean,
  default: false
},
ChildrenOpenActiveRoute: {
  type: Boolean,
  default: true
},
checkButtonActive: {
  type: Boolean,
  default: true
},
vueRouterEnabel: {
  type: Boolean,
  default: false
},
BottomMiniMenuBtn: {
  type: Boolean,
  default: true
},
paddingTop: {
  type: String,
  default: '0px'
},
dark: {
  type: Boolean
},
rtl: {
  type: Boolean,
  default: false
}
closeOpenMenuOnHrefPush:{
  type: Boolean,
  default: false
}
4. Slots.

<!--menu items Append icon-->
<template #itemApendIcon="{ icon,isChildrenMenuOpen, active,miniActive }"></template>
<!--menu items label -->
<template #menuItemLabel="{labelName ,isChildrenMenuOpen, active,miniActive}"></template>
<!--menu items Preppend icon-->
<template #itemPrepandIcon="{ icon,isChildrenMenuOpen, active,miniActive }"></template>
<!--menu header item-->
<template #headerItem="{ header }"></template>
<!--menu header at the top of the menu-->
<template #header></template>
<!--menu footer -->
<template #footer></template>
<!--menus bottom toggle btn -->
<template #BottomMiniMenuBtn></template>
5. Events.

@item-click(MenuItem)
@update:collapsed(isCollapsed)
@update:miniMenu(isMiniMenu)
Preview:
Awesome Sidebar Navigation Component For Vue 3
Changelog:
03/01/2023

ADD option to close open menus on router push
Download Details:
Author: amirkian007

Live Demo: https://amirkian007.github.io/vasmenu/#/

Download Link: https://github.com/amirkian007/vue-awesome-sidebar/archive/refs/heads/main.zip

Official Website: https://github.com/amirkian007/vue-awesome-sidebar

Install & Download:
# Yarn
$ yarn add vue-awesome-sidebar

# NPM
$ npm i vue-awesome-sidebar
RELATED POSTS
Off-canvas Burger Menu For Vue-min
Off-canvas Hamburger Menu System For Vue – burger-menu
 Vuejsadmin  April 29, 2020
Tiny Vue Context Menu Component
Tiny Vue Context Menu Component
 Vuejsadmin  March 4, 2017
Pretty Navbar Component For Vue
Pretty Mobile-friendly Navbar Component – navigation-bar
 Vuejsadmin  May 17, 2022
Stripe-like Dropdown Menu For Vue.js - Stripe Menu
Stripe-like Dropdown Menu For Vue.js – Stripe Menu
 Vuejsadmin  October 2, 2022
Multi-level Dock Menu Component For Vue 3
Multi-level Dock Menu Component For Vue 3
 Vuejsadmin  July 15, 2022
navscroll-js
Highlight Menu Items On Scroll – navscroll-js
 Vuejsadmin  November 15, 2017
Tags:side menu
ADD COMMENT
Comment Text*
Name*
Email*
Website
CATEGORIES
Animation	Audio & Video
Carousel	Chart & Graph
Date Time	Form
Framework	Gallery
Image	Layout
Loading	Modal
Navigation	Notification
Others	Pagination
Scroll	Social
Table	Text
Tooltip	UI
RECENT COMPONENTS
Datetime & Date Range Picker For Vue 3
Datetime & Date Range Picker For Vue 3
 August 19, 2023
Interactive Network Graph Visualization Component For Vue 3
Interactive Network Graph Visualization Component For Vue 3
 August 18, 2023
Tiny Input Mask Library For Vue.js - Input Facade
Tiny Input Mask Library For Vue.js – Input Facade
 August 18, 2023
Notification Library For Vue 3
Notification Library For Vue 3
 August 18, 2023
Lazy Load Youtube Videos To Improve Load Speed
Lazy Load Youtube Videos To Improve Load Speed
 August 18, 2023
POPULAR COMPONENTS
Versatile Number Formatting Library For Vue
Versatile Number Formatting Library For Vue
User-friendly Search Input Component Inspired By Github
User-friendly Search Input Component Inspired By Github
Code Diff Plugin
Code Diff Plugin For Vue 3/2
Simple Draggable Gantt Chart For Vue - Ganttastic
Simple Draggable Gantt Chart For Vue – Ganttastic
Minimal PDF Viewer For Vue 3
Minimal PDF Viewer For Vue 3
FEATURED
7 Best Loading/Progress Indicator Libraries For Vue.js (2023 Update)



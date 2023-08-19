const menus = useMenus()
const menu: MenuCollection[] = []

menu.push({
menu_name: "main-menu",

items: [
{
   name: "home",
   label: "Home",
   to: "/home"
},

{
   name: "about"
   label: "About",
   to: "/about"
},

{
   name: "contact",
   label: "Contact Us",
   to: "/contact"
},
]
})
menus.add(menu)
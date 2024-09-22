### Part 3: Creating the Submenu
- A submenu serves as an additional menu for users to select from, and offers more specific context to the top-level menu's options. 
- We will start by using some DOM manipulation techniques to format the submenu before adding interaction to each menu component.

#### All future steps should be completed within the `index.js` file.
1. Select and cache the <nav id="sub-menu"> element in a variable named `subMenuEl`.
2. Set the height subMenuEl element to be "100%".
3. Set the background color of subMenuEl to the value stored in the `--sub-menu-bg` CSS custom property.
4. Add the class of flex-around to the subMenuEl element.

#### Now, change the position of the submenu to temporarily hide it. Later, we will make the submenu appear dynamically based on user interaction:
1. Set the CSS position property of subMenuEl to the value of absolute.
2. Set the CSS top property of subMenuEl to the value of 0.

### Part 4: Adding Menu Interaction

- In order to add submenu links, we will need to restructure the menuLinks array within index.js. Update the menuLinks array to the following:
```javascript
var menuLinks = [
  {text: 'about', href: '/about'},
  {text: 'catalog', href: '#', subLinks: [
    {text: 'all', href: '/catalog/all'},
    {text: 'top selling', href: '/catalog/top'},
    {text: 'search', href: '/catalog/search'},
  ]},
  {text: 'orders', href: '#' , subLinks: [
    {text: 'new', href: '/orders/new'},
    {text: 'pending', href: '/orders/pending'},
    {text: 'history', href: '/orders/history'},
  ]},
  {text: 'account', href: '#', subLinks: [
    {text: 'profile', href: '/account/profile'},
    {text: 'sign out', href: '/account/signout'},
  ]},
];
```

---
title: Blue Eye Icon
description:
---

# Icon

A great component that give you the ability you to create your own custom icons or fontawsome icons .

> We give you a tool to generate and search for fontawsome icons directly. [Icons List](../../guides/fontawesomelist)

# Benefits

- Create you own custome icons which you can control the size of the font icon file.

- No bloatware, one package with one iconset, nothing more nothing less

- Full set of FontAwesome Icons properly updated

- Insanely fast with minimal memory footprint

<p align="center">
 <img src="https://i.imgur.com/GYK34HW.png" />
</p>

## Installation

to install the latest version of `be-button` you only need to run:

```bash
npm install be-icon  --save
```

or

```bash
yarn add be-icon
```

## Installation process

Font Awesome Icons provide three types of free icons set . you can download which type you want or even you can download them all if you want ;) in addtion we have created custom icon font which you can download also.

**Create Custom Font Icons**

> you can use one of the online font icons generator like [Fontello](http://fontello.com/) which we are using in our custom font example.

| Type         | Font Name(Required) | Download                                                                             |
| ------------ | ------------------- | ------------------------------------------------------------------------------------ |
| RegularIcons | fa-regular-400      | [fa-regular-400](https://drive.google.com/open?id=1yq_sJ5le5S1S06msvaO6W16-9Oo7dXfa) |
| SolidIcons   | fa-solid-900        | [fa-solid-900](https://drive.google.com/open?id=18vQUn80hrR3lxTvB1toRE5Kf0pE37eif)   |
| BrandIcons   | fa-brands-400       | [fa-brands-400](https://drive.google.com/open?id=1qJQ0t9ZchUaikh3TYeuIjGQgS3wrjxEW)  |
| Custom Font  | be-font-icon        | [be-font-icon](https://drive.google.com/open?id=18reeFawb37lZrYh-yPNwqNW75ldhdSrc)   |

> next step is to load these fonts into your app , check below example if you are using expo .

```jsx
async function loadResourcesAsync() {
  await Promise.all([
    Font.loadAsync({
      "fa-solid-900": require("./assets/fonts/fa-solid-900.ttf"),
      "fa-regular-400": require("./assets/fonts/fa-solid-900.ttf"),
      "fa-brands-400": require("./assets/fonts/fa-brands-400.ttf"),
      "be-font-icon": require("./assets/fonts/be-font-icon.ttf") // if you want to use Custom font. you can change the name of the font and the file as you want ( only for custom font icon)
    })
  ]);
}
```

> if you want to use your custom font icons, you need to do one extra step to map your fonts icons and inject them to our Dictionary . which is an easy step .

- Create new javascript file ( for example beIcons.js)

- Export your icons object and make sure that you include in the first element : **\_fontFamily: "be-font-icon"** the same name as you used in Font.loadAsync.

- dont forget to add **\u** before each icon code. also icons name should be **camel case**.

```jsx
export default BeIcons = {
  _fontFamily: "be-font-icon",
  unHappy: "\uE802",
  wink: "\uE813",
  fireStation: "\uE817",
  rss: "\uE800",
  githubCircled: "\uE801",
  sound: "\uE804",
  jabber: "\uF317"
};
```

### That's it!

**Examples**

#### Font Awesome Icons :

```jsx
import Icon, { SolidIcons, RegularIcons, BrandIcons } from "be-icon";
---
<Icon icon={SolidIcons.appleAlt} color="#ff9900" style={ {
    padding: 15, textShadowColor: "#ff0000",
    textShadowOffset: { width: -1, height: -1 },
    textShadowRadius: 2
    } } />
<Icon icon={RegularIcons.bellSlash} style={ { padding: 15, fontSize: 30 } } />
<Icon icon={BrandIcons.amazonPay} color="success" size={100} shadow style={ { padding: 15 } } />
```

<img src="https://i.imgur.com/eX6sk3B.jpg" alt="Basic" style="width:150px" />

#### Custom Font icons :

```jsx
import Icon from "be-icon";
import BeIcons from "./beIcons";//check above code of this object
---
<Icon icon={BeIcons.unHappy} style={ { padding: 15, fontSize: 30 } } />
<Icon icon={BeIcons.fireStation} style={ { padding: 15, fontSize: 30 } } />
<Icon icon={BeIcons.sound} style={ { padding: 15, fontSize: 30 } } />
<Icon icon={BeIcons.jabber} style={ { padding: 15, fontSize: 30 } } />
```

<img src="https://i.imgur.com/qoXCiT8.jpg" alt="Basic" style="width:150px" />

### Props

- [`icon`](icon#icon)
- [`color`](icon#color)
- [`size`](icon#size)
- [`shadow`](icon#shadow)
- [`style`](icon#style)

---

# Reference

### `icon`

set the Icon using one of the fontawsome free icons set.

| Type                                 | Required | Default          |
| ------------------------------------ | -------- | ---------------- |
| SolidIcons, RegularIcons, BrandIcons | YES      | SolidIcons.smile |

### `color`

color of the Icon

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | theme   |

### `size`

set the size of the icon , you can instead of using the size prop, you just override the style prop.

| Type   | Required | Default                 |
| ------ | -------- | ----------------------- |
| Number | No       | BETheme.SIZES.ICON_SIZE |

### `shadow`

If true, show shadow effect for this component.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `style`

override Icon style,since we are using text to render icon then you can use all react native text props

| Type  | Required |
| ----- | -------- |
| style | No       |

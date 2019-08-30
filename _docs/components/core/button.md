---
title: Button
description: How to add interactive quizzes to your site.
---

# Button

An advance button component that should render nicely on any platform. Supports a great level of customization.

<p align="center">
 <img src="https://i.imgur.com/JjkraTc.png" />
</p>

**Examples**

> Basic :

```jsx
import Button from "be-button";
---
<Button onPress={() => console.log("Button Pressed")}>
    Learn More
</Button>
```

<img src="https://i.imgur.com/eDTf1Wn.jpg" alt="Basic" style="width:150px" />

> Outline :

```jsx
import Button from "be-button";
---
<Button outline onPress={() => console.log("Button Pressed")}>
    Learn More
</Button>
```

<img src="https://i.imgur.com/hDVY5m3.jpg" alt="Basic" style="width:150px" />

> advance :

```jsx
import Button from "be-button";
---
 <Button
    color="error"
    textColor="black"
    textStyle={ { fontSize: 30 } }
    containerStyle={ { padding: 60, borderStyle: "dashed" } }
    borderColor="#666"
    borderWidth={6}
    radius={25}
    opacity={0.5}
    textTransform="uppercase"
    onPress={() => console.log("Button Pressed")}
    >
    Learn More
</Button>
```

<img src="https://i.imgur.com/CoGNUtO.jpg" alt="Basic" style="width:150px" />

> With Icon :

```jsx
import Button from "be-button";
import Icon, { RegularIcons } from "be-icon";
---
<Button
    icon={<Icon icon={RegularIcons.smileWink} style={ { paddingRight: 10 } } />}
    color="transparent"
    containerStyle={ {  width: "100%", height: 100 } }
    borderColor="primary"
    borderWidth={1}
    textColor="primary"
    onPress={() => console.log("Button Pressed")}
    >
    NICE !!
</Button>
```

<img src="https://i.imgur.com/iAxBFsU.jpg" alt="Basic" style="width:350px" />

> loading :

```jsx
import Button from "be-button";
---
<Button
    loading
    loadingColor="error"
    loadingSize="large"
    color="transparent"
    containerStyle={ { borderStyle: "dashed" } }
    borderColor="error"
    borderWidth={1}
    radius={40}
    onPress={() => console.log("Button Pressed")}
/>
```

<img src="https://i.imgur.com/oBKCU3r.jpg" alt="Basic" style="width:150px" />

> Custom Content :

```jsx
import Button from "be-button";
import { Image } from "react-native";
---
<Button
    color="transparent"
    containerStyle={ { width: 100, height: 100 } }
    borderColor="#ff9900"
    borderWidth={1}
    onPress={() => console.log("Button Pressed")}
    >
    <Image style={ { width: 50, height: 50 } } source={ { uri: "https://i.imgur.com/Ksp1jHy.png" } } />
</Button>
```

<img src="https://i.imgur.com/CPxohym.jpg" alt="Basic" style="width:150px" />

### Props

- [`onPress`](button#onpress)
- [`color`](button#color)
- [`textColor`](button#textcolor)
- [`borderColor`](button#bordercolor)
- [`borderWidth`](button#borderwidth)
- [`radius`](button#radius)
- [`disabled`](button#disabled)
- [`shadow`](button#shadow)
- [`outline`](button#outline)
- [`opacity`](button#opacity)
- [`loading`](button#loading)
- [`loadingColor`](button#loadingcolor)
- [`loadingSize`](button#loadingsize)

---

# Reference

### `onPress`

Handler to be called when the user taps the button

| Type     | Required |
| -------- | -------- |
| function | Yes      |

### `color`

Background color of the button

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | primary |

### `textColor`

Text color of the button ( only if the children is string)

| Type                                     | Required | Default                                        |
| ---------------------------------------- | -------- | ---------------------------------------------- |
| [be-color](../../guides/color-reference) | No       | white in default case, primary in outline mode |

### `borderColor`

border color of the button , will active if the borderWidth prop great than 0 or the button outline prop set to true

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | primary |

### `borderWidth`

border width of the button you can change border style using containerStyle prop

| Type   | Required | Default                    |
| ------ | -------- | -------------------------- |
| Number | No       | BETheme.SIZES.BORDER_WIDTH |

### `radius`

Button border radius of the button to make it circle you need to set width = height & radius = button width / 2

| Type   | Required | Default                     |
| ------ | -------- | --------------------------- |
| Number | No       | BETheme.SIZES.BORDER_RADIUS |

### `disabled`

If true, disable all interactions for this component.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `shadow`

If true, show shadow effect for this component.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `outline`

If true make an outline button,by set the default text color to primary set background color to transparent and finally set border width to 1, you can ovveride these styles.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `opacity`

Determines what the opacity of the Button should be when touch is active.

| Type   | Required | Default               |
| ------ | -------- | --------------------- |
| Number | No       | BETheme.SIZES.OPACITY |

### `loading`

If true we show react native activity indicator instead of the button content.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `loadingColor`

set Loading indicator color , will active if loading prop set to true

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | primary |

### `loadingSize`

Size of the indicator (default is 'small'). Passing a number to the size prop is only supported on Android.

| Type                          | Required | Default |
| ----------------------------- | -------- | ------- |
| enum('small', 'large'),number | No       | small   |

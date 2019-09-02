---
title: Blue Eye Radio
description:
---

# Radio

An advance Radio component that should render nicely on any platform. Supports a great level of customization.

<p align="center">
 <img src="https://i.imgur.com/4V6s8cy.jpg" />
</p>

## Installation

to install the latest version of `be-radio` you only need to run:

> this package incluse also : **(Radio, Switch, CheckBox, RadioGroup, CheckboxGroup )**

```bash
npm install be-radio --save
```

or

```bash
yarn add be-radio
```

**Examples**

#### Basic

```jsx
import { Radio } from "be-radio";
---
<Radio
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}>
  Nice Radio :)
</Radio>
```

<img src="https://i.imgur.com/X4mMpT4.jpg" alt="Basic" style="width:250px" />

#### Advance

```jsx
import { Radio } from "be-radio";
---
<Radio
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}
  hideIconBorder={true}
  size={60}
  iconActiveColor="success"
  textActiveColor="#00ff00"
  textStyle={ { fontSize: 18 } }>
  active Radio :)
</Radio>
<Radio
  id="2"
  value="10"
  onChange={event => {
    console.log(event);
  }}
  checked={false}
  hideInActiveIcon={false}
  hideLable={false}
  size={30}
  iconInActiveColor="red"
  textInActiveColor="theme"
  textStyle={ { fontSize: 14 } }
  iconStyle={ { borderRadius: 0 } }
  style={ { borderWidth: 1, borderColor: "#ff9900", padding: 5 } }>
  inactive Radio :(
</Radio>
```

<img src="https://i.imgur.com/Ris5hpn.jpg" alt="Basic" style="width:250px" />

#### advance

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

#### With Icon

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

#### loading

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

#### Custom Content

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

#### TouchableHighlight

```jsx
import Button from "be-button";
import { Image } from "react-native";
---
<Button
    type="TouchableHighlight"
    opacity={1}
    onShowUnderlay={() =>
    <Image style={ { width: 50, height: 50 } } source={ { uri: "https://i.imgur.com/dNSN9D7.png" } } />}
    underlayStyle={ { width: 105, height: 105 } }
    containerStyle={ { width: 100, height: 100 } }
    borderColor="#ff9900"
    underlayColor="success"
    borderWidth={1}
    onPress={() => console.log("Button Pressed")}
    >
    <Image style={ { width: 50, height: 50 } } source={ { uri: "https://i.imgur.com/LgkZkOG.png" } } />
</Button>
```

<table  style="border: none !important;">
<tr><td style="width:200px">Unpressed </td><td>Pressed</td></tr>
<tr><td>
<img src="https://i.imgur.com/FaNgc3z.jpg" alt="Basic" style="width:100px" />
</td><td>
<img src="https://i.imgur.com/42ECqBb.jpg" alt="Basic" style="width:100px" />
</td></tr>
</table>

### Props

- [`onPress`](button#onpress)
- [`type`](button#type)
- [`containerStyle`](button#containerstyle)
- [`color`](button#color)
- [`textColor`](button#textcolor)
- [`textTransform`](button#texttransform)
- [`textStyle`](button#textstyle)
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
- [`underlayColor`](button#underlaycolor)
- [`underlayStyle`](button#underlaystyle)

---

# Reference

### `onPress`

Handler to be called when the user taps the button

| Type     | Required |
| -------- | -------- |
| function | Yes      |

### `type`

**TouchableOpacity** selected by default, so when press Button down, the opacity of the wrapped view is decreased, dimming it.
if you want to change the background color or even the entire component when you press the button down then you need to change the type to **TouchableHighlight**

| Type                                | Required | Default          |
| ----------------------------------- | -------- | ---------------- |
| TouchableOpacity,TouchableHighlight | No       | TouchableOpacity |

### `containerStyle`

override button container style for example if you want to change width,height,padding,....

| Type  | Required |
| ----- | -------- |
| style | No       |

### `color`

Background color of the button

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | theme   |

### `textColor`

Text color of the button ( only if the children is string)

| Type                                     | Required | Default                                        |
| ---------------------------------------- | -------- | ---------------------------------------------- |
| [be-color](../../guides/color-reference) | No       | white in default case, primary in outline mode |

### `textTransform`

set Text Transform ( only if the children is string)

| Type                                  | Required | Default |
| ------------------------------------- | -------- | ------- |
| 'lowercase', 'uppercase','capitalize' | No       | Not Set |

### `textStyle`

override button text style for example if you want to change fontSize,... ( only if the children is string)

| Type  | Required |
| ----- | -------- |
| style | No       |

### `borderColor`

border color of the button , will active if the borderWidth prop great than 0 or the button outline prop set to true

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | theme   |

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
| [be-color](../../guides/color-reference) | No       | theme   |

### `loadingSize`

Size of the indicator (default is 'small'). Passing a number to the size prop is only supported on Android.

| Type                          | Required | Default |
| ----------------------------- | -------- | ------- |
| enum('small', 'large'),number | No       | small   |

### `underlayColor`

Background color of the button when pressed , only if the button type is **TouchableHighlight**

| Type                                     | Required | Default |
| ---------------------------------------- | -------- | ------- |
| [be-color](../../guides/color-reference) | No       | theme   |

### `underlayStyle`

override button container style when pressed **this will keep the container styles and push the new style** , only if the button type is **TouchableHighlight**

| Type  | Required |
| ----- | -------- |
| style | No       |

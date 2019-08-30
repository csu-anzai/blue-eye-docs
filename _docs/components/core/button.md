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

![Kiku](../../../assets/img/logo.png)

> Outline :

```jsx
import Button from "be-button";
---
<Button outline onPress={() => console.log("Button Pressed")}>
    Learn More
</Button>
```

![Kiku](../../../assets/img/logo.png)

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

![Kiku](../../../assets/img/logo.png)

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

![Kiku](../../../assets/img/logo.png)

### Props

- [`accessibilityLabel`](button.md#accessibilitylabel)
- [`color`](button.md#color)
- [`disabled`](button.md#disabled)
- [`hasTVPreferredFocus`](button.md#hastvpreferredfocus)
- [`nextFocusDown`](button.md#nextfocusdown)
- [`nextFocusForward`](button.md#nextfocusForward)
- [`nextFocusLeft`](button.md#nextfocusleft)
- [`nextFocusRight`](button.md#nextfocusright)
- [`nextFocusUp`](button.md#nextfocusleft)
- [`onPress`](button#onpress)
- [`testID`](button.md#testid)
- [`title`](button.md#title)
- [`touchSoundDisabled`](button.md#touchSoundDisabled)

---

# Reference

## Props

### `onPress`

Handler to be called when the user taps the button

| Type     | Required |
| -------- | -------- |
| function | Yes      |

### `hi`

Handler to be called when the user taps the button

| Type     | Required |
| -------- | -------- |
| function | Yes      |

---

|             Prop              |     Type     |      Default       |                                             Description                                              |
| :---------------------------: | :----------: | :----------------: | :--------------------------------------------------------------------------------------------------: |
| ...TouchableOpacity.propTypes |              |                    |                                                                                                      |
|          capitalize           |     bool     |       false        |                          Transforms the first character in a capital letter                          |
|             color             |    string    |     'primary'      | your options are: 'primary', 'theme', 'error', 'warning', 'succes', 'transparent' or your own color  |
|           disabled            |     bool     |       false        |                                         Disables the button                                          |
|             icon              | bool, string |       false        |                            pick whatever icon you want from Expo's icons                             |
|           iconColor           | bool, string | theme.COLORS.BLACK |                                        sets the icon's color                                         |
|          iconFamily           | bool, string |       false        |                 pick whatever icon family suits the icon you chose from Expo's icons                 |
|           iconSize            |    number    |         14         |                                         sets the icon's size                                         |
|            loading            |     bool     |       false        |                        Uses the <ActivityIndicator /> for the loading effect                         |
|          loadingSize          |    string    |      'small'       |                                  your options are: 'small', 'large'                                  |
|           lowercase           |     bool     |       false        |                                     makes all letters lowercase                                      |
|           onlyIcon            |     bool     |       false        |                     adds specific styling for using only an icon in your button                      |
|            opacity            |    number    |        0.8         |                                     changes the button's opacity                                     |
|            radius             |    number    |         0          |                                     changes the button's radius                                      |
|          shadowColor          | bool, string |       false        | the default shadowColor is based on the button's color but you can also write a specific shadowColor |
|          shadowless           |     bool     |       false        |                                            removes shadow                                            |
|             size              |    number    |      'large'       |                                  your options are: 'large', 'small'                                  |
|           uppercase           |     bool     |       false        |                                     makes all letters uppercase                                      |

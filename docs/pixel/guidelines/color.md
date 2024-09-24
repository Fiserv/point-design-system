# Color
## Overview

The default themes are derived from the design system's color palette. The slate blue family is dominant in the default themes, making use of subtle shifts in value to organize content into distinct zones. The core blue family serves as the primary action color across all Fiserv products and experiences. Additional colors are used sparingly and purposefully.

Colors in the neutral gray palette are layered on top of each other to create depth and spatial associations. The layering model defines the logic of how colors stack on top of each other in a UI when using the Pixel theming capabilities. Aspects of the layering model are built directly into the themes, color tokens, and components.

The layering model differs between the light and dark themes.

- In the light themes, layers alternate between $white and $slate_50 with each added layer.
- In the dark themes, layers become one step lighter with each added layer.

### Implementing color

This Pixel uses tokens and themes to manage color. Tokens are role-based, and themes specify the color values that serve those roles in the UI.

| Term | Definition |
|:---|:---|
| Theme | A theme is a collection of colors designed to create a specific aesthetic. Themes control the color value assigned to a token.|
| Token | A token is the role-based identifier that assigns a color. Unlike hex codes, tokens apply universally across themes. For example, $layer_1, $border_subtle, $support_error.|
| Role | A role is the systematic usage of a color assigned to a token. Roles cannot be changed between themes.|
| Value | A value is the unique visual attribute (hex code, rgba value) assigned to a token through the use of themes.

### Themes

Themes serve as an organizational framework for color in Pixel, with each theme based on a specific primary background color. And they actually get their names from their background color. There are two default light themes and dark themes.

The light themes are based on $white and $slate_50 backgrounds, and the dark themes use $black and $gray_900 backgrounds. Within each theme, the values for the universal color tokens use the primary background color as the base of its layering model.

### Global background colors

| Palette Token | Primary Background.     | Color Token | Value   |
|:--------------|:------------------------|:------------|:--------|
| $white        | Global background light | $background | #FFFFFF |
| $slate_50     | Global background light | $background | #EEF2F6 |
| $black        | Global background dark  | $background | #000000 |
| $gray_900     | Global background dark  | $background | #212121 |

### Light themes

There are two light themes in the Pixel design system: $white and $slate_50. For enabled UI color's light themes primarily use the color range of $white to $gray_200, and for text and icons uses the color range between $gray_900 and $gray_600.

#### Layering model

In the light themes, layers alternate between White and Gray.

- **White theme:** uses $white as the global background color and is layered first with components using $slate_50 backgrounds. The second layer uses $white, and the third layer used $slate_50.
- **Slate_50 theme:** uses $slate_50 as the global background color and is layered first with components using $white backgrounds. The second layer uses $slate_50 and the third layer used $white.

### Dark themes

There are two dark themes in the Pixel design system: Black and Gray 900. For enabled UI colors, dark themes primarily use the color range of Gray 900 through Black, and for text and icons uses the color range between White and Gray 500.

#### Layering model

- **Gray 900 theme:** uses $gray_900 as the global background color and is layered first with components using $black backgrounds. The second layer uses $gray_900, and the third layer used $black.
- **Black theme:** uses $black as the global background color and is layered first with components using $gray_900 backgrounds. The second layer uses $gray_800 and the third layer used $gray_700.

### High contrast monments

In some cases, it is helpful to apply light components to dark backgrounds or dark components to light backgrounds. This technique is useful to focus attention or create visual tension. Some high contrast moments are baked into the themes by using the inverse tokens, like the tooltip component. Other times high contrast moments can be achieved through applying inline theming for instances like a dark header with a light theme page.

### Tokens

Tokens are method of applying color in a consistent, reusable, and scalable way. They help us abstract how we use color from the values themselves. They are used in place of hard coded values, like hex codes. Tokens allow for value changes to be made at scale, making design language changes easy to implement, as well as making possible color functionalities like inline theming and light or dark mode.

Each token is assigned a role and a value. The role determines what element to apply a token too and the value is the actual color (hex code) that appears in the assigned theme. Color token names and roles are the same across themes, only the assigned value will change with the theme. For example, under the hood the `$text_secondary`token can dynamically map to `$gray_900` or `$black` depending on the theme.

For quick reference, the role of a token is represented in the token name itself to help you correctly apply tokens. The first part of the token name references the general UI element the color is being applied to, like background, text, or border. The second part of token name will specify its unique role within the element group like `$border_subtle` or `$text_primary`. Additionally, some tokens include an interaction state at the end, like `$background_hover`.

### Core tokens
Color tokens that can be applied across components are called core tokens. There are ten main groups of core color tokens. They are grouped by the common UI element that they are applied to. Token groups makes it easier to find and apply color tokens. Interaction state tokens are included in the group alongside their enabled state tokens. There are a few core tokens that do not belong to a group and stand as individual tokens like `$overlay`, `$highlight`, and `$interactive`.

| Token group   | Applied to   																		   |
| :------------ | :----------------------------------------------------------------------------------- |
| Background    | Page or primary backgrounds.                                                         |
| Button        | Button and navigation.                                                               |
| Layers        | Stacked backgrounds (includes layering tokens).                                      |
| Field         | Form and input backgrounds (includes layering tokens).                               |
| Border        | Dividers, rules, and borders between and around elements (includes layering tokens). |
| Text          | Type and type styles.                                                                |
| Link          | Standalone and inline links. 														   |
| Icon          | Icons and pictograms.               												   |
| Support       | Notification elements and status indicators.                                         |
| Focus         | Focus states.																		   |
| Skeleton      | Skeleton states.																	   |

### Component tokens

Some components have their own specific color tokens, known as component tokens. They represent the properties associated with a particular component. They are not global tokens like the core tokens and should never be used for anything other than their own component.

### Interaction states

In addition to the core set of enabled-state tokens, there are five other interaction states defined with tokens for each theme. Interaction tokens are signified by the addition of a state name added to the end of the base token name. For example, the $background hover state token is $background_hover.

The color layering model for interaction tokens is as follows:

- For values between $black and $slate_700, interaction gets lighter.
- For values between $slate_600 and $white, interaction gets darker.

#### Hover
Hover is a subtle visual change that appears when a mouse cursor moves over an interactive element. Hover states have their own tokens and are identified by `_hover` added to the end of the base token name, such as `$background_hover`.

In the themes, hover states token values are “half steps” between two adjacent colors on the Pixel core color palette steps. These values fall outside of the core color palette steps and have their own spectrum. Hover colors should not be used for anything other hover states.

- For values between $black and $slate_700, the hover state is a half-step lighter.
- For values between $slate_600 and $white, the hover state is a half-step darker.

Elements like text or icons that use secondary colors for their enabled state, will change to the primary color on hover, giving them a subtle emphasis. Most of the time, this shift in color (on the text or icon element) will be accompanied by a background hover color shift as well. For example, an overflow menu uses `$text_secondary` and `$layer_1` in its enabled state. On hover, the text switches to `$text_primary `and the background to `$layer_hover_1`.

#### Active

The active state can be used to indicate a click, tap or down press of a button. Active tokens are identified by `_active` added after the base token name, such as $button_primary_active. Active state values are two full steps lighter or darker on the color scale.

- For values between 100 and 70, the active state is two full steps lighter.
- For values between 60 and 10, the active state is two full steps darker.

#### Selected

Selected states indicate item(s) or option(s) that have been chosen in the UI by the user through any input method. Selected tokens are identified by the `_selected `added after base token name, such as $layer_selected_1. The color logic for selected state is either one full step lighter or darker on the color scale.

- For values between $black and $slate_700, the selected state is one full step lighter.
- For values between $slate_600 and $slate_50, the selected state one full step darker.

The exception is that $white shares the same selected state value as $slate_50, and Black shares the same selected state value as $slate_900.

Elements like text or icons that use secondary colors for their enabled state, will change to the primary color when selected, giving them a subtle emphasis. Most of the time, this shift in color (to the text or icon element) will be accompanied by a selected background color shift as well.

#### Focus

The focus state draws attention to the active element on a page when using the keyboard or voice to navigate. In the Pixel design system, the focus of an element is most commonly indicated by a 1px border around the element. In order to make it easy to identify and locate on a page, most focus states use only one color per theme controlled through the $focus color token.

- In the light themes, the focus state usually appears as a $blue_800 border.
- In the dark themes, the focus state usually appears as a $white border.
- The exception is high contrast moments where a $focus_inverse color is used instead.

Focus states are required on all interactive elements and must pass 3:1 color contrast accessibility. Often times to achieve proper 3:1 contrast a $focus_inset border is used between the focus border and the element itself.

#### Disabled

A disabled state is applied to a component when the user is not allowed to interact with the component due to either permissions, dependencies, or pre-requisites. Disabled states completely remove the interactive function of a component and therefore don’t receive hover or focus. Disabled state styling is not subject to WC3 contrast compliance standards and is intentionally de-emphasized in a faded fashion.

Disabled elements are always styled in the Gray family no matter its base color. A component’s specific styling will depend on the elements within it and what layers they are placed on. Some tokens have their own specific disabled tokens, such as `$layer_disabled`, while other elements are grouped together and share a disabled token like $text_disabled.

- For the light themes, disabled color values range from $white to $gray_500
- For the dark themes, disabled color values range from $gray_900 to $gray_400

### Contrast ratios

Contrast is the difference in brightness between any two elements. The [Web Content Acessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG21/) set specific ratios that achieve the minimum required contrast for legibility. Generally speaking, small text is any size below 24px and requires a 4.5:1 contrast ratio. Large text is anything above 24px and requires a 3:1 contrast ratio. Graphical elements, such as data visualizations, also require a 3:1 contrast ratio.

The Pixel design system palette is comprised of twelve color grades—Black, White and ten values for each hue. The following table indicates the minimum number of steps required to achieve commonly used contrast ratios between any two colors.

| Color 1 - Base | Color 2 - 04.05:1           | Color 3 - 00.03:1           |
| :------------- | :-------------------------- | :-------------------------- |
| Black          | 500 through white (6 steps) | 600 through white (5 steps) |
| Gray 900       | 500 through white (4 steps) | 600 through white (3 steps) |
| Gray 800       | 400 through white (4 steps) | 500 through white (3 steps) |
| Gray 700       | 300 through white (4 steps) | 400 through white (3 steps) |
| Gray 600       | 500 through white (4 steps) | 200 through white (3 steps) |
| Gray 500       | 900 through Black (4 steps) | 800 through Black (3 steps) |
| Gray 400       | 800 through Black (4 steps) | 700 through Black (3 steps) |
| Gray 300       | 700 through Black (5 steps) | 700 through Black (4 steps) |
| Gray 200       | 700 through Black (5 steps) | 600 through Black (3 steps) |
| Gray 100       | 600 through Black (5 steps) | 500 through Black (4 steps) |
| White          | 600 through Black (6 steps) | 500 through Black (5 steps) |

## Implementation

### Layering

There are two ways to implement the layering model in a theme, either by using explicit tokens or contextual tokens. These techniques can be used independently in a product or can be used together. Both methods produce the same visual result, the difference lays in how you develop with them. Designers only need to be concerned with the layering tokens.

The explicit layering tokens are standard design tokens. Each layering token corresponds to a specific layer on the page and is used exactly like any other token from design system. Contextual tokens are a special case of layering tokens where the value changes depending on where the token is used on a page. This type of token is incredibly useful for building reusable components that work across layers.

| Token type        | Definition                  																											   |
| :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| Layering tokens   | Explicit layering tokens used to manually map the layering model onto components. They come in sets that pair with individual UI layers. |
| Contextual tokens | Abstract code tokens used to automatically map the layering model onto components depending on where it used on the page.                |

### Layering tokens

Layering tokens are explicit tokens used to manually map the layering model onto components. They are used just like any other color token. Layering tokens come in predefined sets that coordinate with the different layer levels. For each layer that a component needs to lives on a separate component variation must be built using the tokens from that layer set.

#### When to use layering tokens

- As an easy starting point when first working with the layering model, they are exactly like the tokens you already know and love
- When building components that may only need to be on one layer or have only one-color variant.

#### How layering tokens work

There are four layers within a theme: base `layer_0`, `layer_1`, `layer_2`, and `layer_3`. Layers stack one on top of the other in a set order. Each step in UI color (excluding interaction colors) is another layer and will require the use of a different set of layering tokens.

#### Layer sets
Layering tokens are divided into sets and are identified by a number `(_0,_1,_2,_3)` attached to the end of token name. Any token with an `_01` ending belongs to the 01 layering set and so on. The exception are tokens in the base set which use background tokens without a number ending as well as tokens with `_0` classification.

Tokens from the same set are used together when building components. For example, in a dropdown both the input and menu will use tokens from the same set (see image below). In addition to the $layer tokens, layer sets also include border and field tokens, as well as interactive states tokens. A field is considered a layer on top of the background it is placed on, for example a field placed on a `$layer-02` background will use `$field_3`. Border tokens however, pair with its same number, for example `$field_3` pairs with `$border_strong_3` in a text input.

#### Applying layering tokens in a layout

Referencing the image below, the starting base layer is the page area behind and above the tabs; it uses $background from the base set. The tab component is layered on top of the page background to create the first layer. The selected tab uses `$layer_1` and the unselected tabs use `$layer_accent_1` which is not considered a proper layer but a supporting color for $layer inside of components. The tab content area attached to the selected tab is also only one layer above the base and so also uses `$layer_1` as its background.

In the tab’s main section, the text input field is placed on top of `$layer_1` making it a part of the next layer level and will use tokens from the `_2` layer set, so `$field_2` and `$border_strong_2`. Also, a part of the second layer level are the cards in the sub-section which includes the card background `$layer_2` as well as the border between the cards `$border_subtle_2`. However, components added on top of the cards—the text input and overflow menu—are considered part of third layer level and will use tokens from the `_3` layer set.

#### Building components with layer tokens

Building components with layering tokens works just like how you would have always built component color variations in the Pixel design system. For each layer that a component lives on, a separate component variation must be built using the tokens from that layering set.

Spec each component variant with its corresponding layering set. For elements that are not part of the layer sets like type or icons, apply color tokens as you normally would. Non-layer tokens will be the same across variants because they have enough contrast not to need a change with each layer.

### Contextual tokens

Contextual tokens are code specific tokens used to automatically map the layering model onto components depending on where it used on the page. A contextual token is aware of what layer it is placed on and will call the correct values for that layer. There is only one set of contextual tokens, and they require only one component variant to be built.

Contextual tokens can be used in place of layering tokens. The two types of tokens have similar token names except the contextual tokens do not have the number terminal. Contextual tokens keep the same name no matter which layer it sits on.

#### When to use contextual tokens

When building reusable components that need to work across layers.

#### How contextual tokens work

Layering is still possible using the contextual tokens. However, the value of the token is not fixed per theme like with a normal design token from the layering sets. Contextual tokens have a variable value within a theme that is controlled through the use of a special component called the layer component.

#### Using the layer component

The layer component is used to render a single component on different layers. Components built with contextual tokens when placed inside the layer component will automatically map to the correct layer based on where it sits in the layer structure. Components can be nested inside the layer component up to three level, the last level corresponding to the 03 layer set tokens. By default, tokens use the `_1` layer set tokens in the first layer.

#### Applying contextual layer tokens in a layout

When applying contextual tokens, there are no layer sets so each layer uses the same tokens but will be wrapped in a different level of the layer component.

### Building components with contextual tokens

Build a single component as you would normally but apply the contextual color tokens instead of the layer set tokens. Then in your product code wrap the component in the layer component to express the nested layer visuals. Even if the component is never used at other layer levels it is still acceptable and encouraged to use the contextual tokens.

#### Designing for contextual tokens

Contextual tokens are only available in code and are not a part of the design assets. Designers should use the layer set tokens when creating assets but can include contextual tokens in their specs and redlines. To convert a layer set token to a contextual token, simply drop the numbers at the end of the token name.

### Inline theming

Inline theming is used when a section of a UI needs to be a different theme from the rest of the page. Inline theming allows themes to be nested within each other without needing custom styles or overrides.

In product, a common use-case for inline theming is applying a contrasting theme to the UI Shell or side panels. This is especially common in light themed products or light modes. For example, the majority of a page may use the white theme while the UI Shell and the right-side panels use an inline dark theme. This type of theme pairing creates a high contrast moment that can add emphasis and focus to a work flow.

#### When to use inline theming

Only use inline theming for major shifts in color, like high contrast moments. The more subtle transitions of color in a product are handled within each theme through the layering model tokens. It is unlikely that you’ll need to inline a white theme within the dark theme.

#### How inline theming works

In order to implement inline theming, you must use the design system color tokens and themes. For the section of the product, you want to inline theme, simply apply the core design system tokens like you were doing for the rest of the page, then wrap the targeted section in the Theme component to assign a new theme.

#### Designing for inline theming

When designing for inline theming, you’ll need to pull assets that you want in your frame from other library files in your DSK. Assets will have the same token names across libraries but will show different values. Specify in the design deliverables which sections of the page will be using an inline theme.

> [!Note]
> Figma's variable tool helps manage the inline themes by selecting the component and toggling the theme you want.

### Light or dark mode

Light or dark mode is a theme setting that allows the end user to choose either an UI that is predominately light or dark in color. The UI will automatically switch from using light colors backgrounds with dark color text to using dark color backgrounds with light color text.

#### When to use modes

Adding the ability to change between a light or dark mode in your product is not required as a Fiserv product but is highly encouraged especially with whitelabelled software that needs to reflect client's brand. Attention to detail, customization, and being at the forefront of innovation separates over our competitors.

#### Respecting our users' preferences

Most operating system nowadays (ex: MacOS, iOS, in Windows, Android and Linux/GNOME 3) support dark and light modes, offering APIs so that websites and application can automatically match users preferred mode. Many users prefer working on dark themed IDEs and using dark mode in their machines.

#### Creating optimal user conditions

For some users, choosing light versus dark mode is more than an aesthetic choice. While some [research](https://www.nngroup.com/articles/dark-mode/) shows that unimpaired sighted user perform better in light mode, it also shows that dark mode is better for people with cataract and related disorders. Dark mode emits less light and can therefor reduces eyes strain and help prevent headaches and migraine.

#### How modes work

The themes use color tokens to interpret which values are needed for each theme. It is the color tokens that allows a UI to so easily switch from one mode to the next. You cannot implement light or dark mode without using color tokens everywhere in your product. Hard coded values will not change when the mode is switched.

### Designing for modes

You can build a light or dark mode by using the design system themes and color tokens. Your product will need to choose a light theme (White or Slate) and a dark theme (Black or Gray 900). All color in your designs and components should be redlined using the design system color tokens (it would also be to your advantage to use the color token layer styles from the design asset libraries when designing).

Redlining a design in one theme should be enough and not require duplicate designs. However, products teams may want to have design comps in multiple themes. In Figma, we recommend that you duplicate your files, then swap your current theme library for another. This replaces local instances with matching instances from the other library. For step-by-step instructions, visit this [Figma tutorial](https://help.figma.com/hc/en-us/articles/4404856784663-Swap-style-and-component-libraries).

#### Creating a mode control

Since this is a user preference, you’ll need to add a control somewhere in your product for the user to make a theme mode selection. This is commonly done in a display setting, user profile, or account area. At the moment, the placement and design of this control is up to product teams, further guidance and designs for a mode control in Fiserv products may be offered in the future.

#### Inline themes with modes

Mixing themes inline is still allowed with light or dark mode. Mixing inline theme contrast between elements in different modes is also allowed. It is very common for products to have side panels or UI shell elements be high contrast in light mode but low contrast in dark mode. These relationships can be mapped in code using the theme component. Note that smaller components built with an inverse tokens (like tooltip) should remain high contrast when switching modes.

## Core color tokens

The color tokens help you control the visual layer of your system’s components at the atom level for global consistency. Depending on the components defined in your initial system, the maturity of this template can include any additional components or attributes in the future.

The tokens should function as a common language during the product cycle. It is critical that the naming convention should be agreed upon between both development and design. Some tokens values can remain empty, using the token as a placeholder for other themes.

### Background

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$background`                   | '$white'              | '$black'              |
| `$background_brand `            | '$orange_500'         | '$oranage_500'        |
| `$background_hover `            |                       |                       |
| `$background_inverse`           |                       |                       |
| `$background_inverse_hover`     |                       |                       |
| `$background_active`            |                       |                       |
| `$background_active_hover`      |                       |                       |
| `$background_selected`          |                       |                       |
| `$background_seected_hover`     |                       |                       |


### Border

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$border_interactive`           | '$blue_800'           | '$blue_600'           |
| `$border_subtle_1 `             | '$gray_300'           | '$gray_800'           |
| `$border_subtle_2`              |                       |                       |
| `$border_subtle_3 `             |                       |                       |
| `$border_subtle_selected_1 `    |                       |                       |
| `$border_subtle_selected_2 `    |                       |                       |
| `$border_subtle_selected_3`     |                       |                       |
| `$border_strong_1`              | '$gray_400'           | '$gray_600'           |
| `$border_strong_2`              |                       |                       |
| `$border_strong_3`              |                       |                       |
| `$border_strong_selected_1`     |                       |                       |
| `$border_strong_selected_2`     |                       |                       |
| `$border_strong_selected_3`     |                       |                       |
| `$border_card_1`                |                       |                       |
| `$border_card_2`                |                       |                       |
| `$border_card_3`                |                       |                       |
| `$border_inverse`               | '$gray_700'           | '$gray_100'           |
| `$border_disabled`              | '$gray_300'           | '$gray_500'           |

### Button

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$button_primary`               | '$blue_800'           | '$blue_600'           |
| `$button_primary_hover`         | '$blue_700'           | '$blue_500'           |
| `$button_primary_active`        |                       |                       |
| `$button_primary_selected`      | '$blue_900'           | '$blue_800'           |
| `$button_secondary`             | '$blue_800'           | '$white'              |
| `$button_secondary_hover`       | '$blue_700'           | 'rgba($white,.25)'    |
| `$button_secondary_active`      |                       |                       |
| `$button_secondary_selected`    | '$blue_900'           | 'rgba($white,.25)'    |
| `$button_tertiary`              | 'rgba($blue_800,.00)' | 'rgba($white,.00)'    |
| `$button_tertiary_hover`        | 'rgba($blue_800'.25)' | 'rgba($white,.25)'    |
| `$button_tertiary_active`       |                       |                       |
| `$button_tertiary_selected`     | 'rgba($blue_800'.25)' | 'rgba($white,.25)'    |
| `$button_danger`                | '$red_800'            | '$red_700'            |
| `$button_danger_hover`          | '$red_700'            | '$red_600'            |
| `$button_danger_active`         |                       |                       |
| `$button_danger_selected`       | '$red_400'            | '$red_900'            |
| `$button_seperator`             |                       |                       |
| `$button_danger_selected`       | '$gray_400'           | '$gray_600'           |

### Field

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$field_1`                      | '$white'              | '$black'              |
| `$field_2`                      |                       |                       | 
| `$field_3`                      |                       |                       |
| `$field_hover_1`                |                       |                       |
| `$field_hover_2`                |                       |                       |
| `$field_hover_3`                |                       |                       |
| `$field_disabled_1`             | '$gray_100'           | '$gray_900'           |
| `$field_disabled_2`             |                       |                       |
| `$field_disabled_3`             |                       |                       |
| `$fieldset_1`                   | '$gray_50'            | '$gray_800'           |
| `$fieldset_2`                   |                       |                       |
| `$fieldset_3`                   |                       |                       |

### Focus

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$focus`                        | '$blue_800'           | '$white'              |
| `$focus_highlight`              | '$blue_A100'          | 'rgba($white,.25)'    |
| `$focus_inset`                  |                       |                       |
| `$focus_inverse`                | '$white'              | '$blue_600'           |
| `$focus_inverse_highlight`      | 'rgba($white,.10)'    | 'rgba($blue_600,.10)' |

### Icon

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$icon_primary`                 | '$gray_900'           | '$gray_100'           |
| `$icon_secondary`               | '$gray_700'           | '$gray_300'           |
| `$icon_on_color`                | '$white'              | '$white'              |
| `$icon_on_color_disabled`       | 'rgba($white,.50)'    | 'rgba($white,.50)'    |
| `$icon_interactive`             | '$blue_700'           | '$blue_600'           |
| `$icon_inverse`                 | '$white'              | '$black'              |
| `$icon_disabled`                | '$gray_500'           | 'gray_600'            |

### Layer

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$layer_1`                      | '$white'              | '$gray_900'           |
| `$layer_2`                      | '$slate_50'           | '$gray_800'           |
| `$layer_3`                      | '$white'              | '$gray_900'           |
| `$layer_hover_1`                | '$slate_50'           | '$gray_800'           |
| `$layer_hover_2`                | '$slate_100'          | '$gray_700'           |
| `$layer_hover_3`                | '$slate_50'           | '$gray_600'           |
| `$layer_active_1`               |                       |                       |
| `$layer_active_2`               |                       |                       |
| `$layer_active_3`               |                       |                       |
| `$layer_active_hover_1`         |                       |                       |
| `$layer_active_hover_2`         |                       |                       |
| `$layer_active_hover_3`         |                       |                       |
| `$layer_selected_1`             | '$blue_900'           | '$gray_900'           |
| `$layer_selected_2`             | '$blue_900'           | '$gray_900'           |
| `$layer_selected_3`             | '$blue_900'           | '$gray_900'           |
| `$layer_selected_hover_1`       |                       |                       |
| `$layer_selected_hover_2`       |                       |                       |
| `$layer_selected_hover_3`       |                       |                       |
| `$layer_disabled_1`             | '$gray_100'           |'$gray_800'            |
| `$layer_disabled_2`             |                       |                       |
| `$layer_disabled_3`             |                       |                       |

### Layer accent

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$layer_accent_1`               | '$gray_300'           | '$gray_800'           |
| `$layer_accent_2`               |                       |                       |
| `$layer_accent_3`               |                       |                       |
| `$layer_accent_hover_1`         |                       |                       |
| `$layer_accent_hover_2`         |                       |                       |
| `$layer_accent_hover_3`         |                       |                       |
| `$layer_accent_active_1`        |                       |                       |
| `$layer_accent_active_2`        |                       |                       |
| `$layer_accent_active_3`        |                       |                       |
| `$layer_accent_selected_1`      |                       |                       |
| `$layer_accent_selected_2`      |                       |                       |
| `$layer_accent_selected_3`      |                       |                       |

### Link

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$link_primary`                 | '$blue_700'           | '$blue_400'           |
| `$link_primary_hover`           | '$blue_800'           | '$blue_300'           |
| `$link_primary_active`          |                       |                       |
| `$link_primary_selected`        | '$blue_900'           | '$blue_900'           |
| `$link_secondary`               |                       |                       |
| `$link_secondary_hover`         |                       |                       |
| `$link_secondary_active`        |                       |                       | 
| `$link_secondary_selected`      |                       |                       |
| `$link_inverse`                 | '$blue_500'           | '$blue_600'           |
| `$link_inverse_hover`           |                       |                       |
| `$link_inverse_active`          |                       |                       |
| `$link_inverse_selected`        |                       |                       |
| `$link_visited`                 |                       |                       |
| `$link_disabled`                | '$gray_500'           | '$gray_500'           |

### Support

| Token name                      | Light theme           | Dark theme             |
| :------------------------------ | :-------------------- | :--------------------- |
| `$support_error`                | '$red_800'            | '$red_700'             |
| `$support_error_bg`             | '$red_A100'           | 'rgba($red_700,.10)'   |
| `$support_success`              | '$green_900'          | '$green_700'           |
| `$support_success_bg`           | '$green_A100'         | 'rgba($green_700,.10)' |
| `$support_warning`              | '$orange_500'         | '$orange_400'          |
| `$support_warning_bg`           | '$orange_A100'        | 'rgba($orange_400,.10)'|
| `$support_information`          | '$blue_800'           | '$blue_600'            |
| `$support_information_bg`       | '$blue_A100'          | '$rgba($blue_600,.10)' |

### Text

| Token name                      | Light theme           | Dark theme             |
| :------------------------------ | :-------------------- | :--------------------- |
| `$text_primary`                 | '$gray_900'           | '$gray_100'            |
| `$text_secondary`               | '$gray_700'           | '$gray_300'            |
| `$text_placeholder`             | '$gray_500'           | '$gray_600'            |
| `$text_on_color`                | '$white'              | '$white'               |
| `$text_on_color_disabled`       | '$rgba($white,.50)'   | 'rgba($white,.50)'     | 
| `$text_inverse`                 | '$white'              | '$black'               |
| `$text_disabled`                | '$gray_500'           | '$gray_600'            |

### Miscellaneous

| Token name                      | Light theme           | Dark theme             |
| :------------------------------ | :-------------------- | :--------------------- |
| `$interative`                   | `$blue_800`           | `$blue_600`            |
| `$highlight`                    |                       |                        |
| `$overlay`                      | `rgba($black,.50)`    | `rgba($black,.50)`     |
| `$skeleton_element`             | `$gray_400`           | `$gray_800`            |
| `$skeleton_background`          | `$gray_200`           | `gray_900`             |


## Palette token

### Black and White

| Token name            | Background                                                                                     | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :--------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$black`              | <img valign='middle' alt='amber_900' src='https://readme-swatches.vercel.app/000000'/> #000000 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 21.01:1              |
| `$white`              | <img valign='middle' alt='amber_800' src='https://readme-swatches.vercel.app/FFFFFF'/> #FFFFFF | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 21.01:1              |

### Gray

| Token name            | Background                                                                                    | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :---------------------------------------------------------------------------------------------| :---------------------------------------------------------------------------------------- | -------------------: | 
| `$gray_900`           | <img valign='middle' alt='gray_900' src='https://readme-swatches.vercel.app/212121'/> #212121 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 16.01:1              |
| `$gray_800`           | <img valign='middle' alt='gray_800' src='https://readme-swatches.vercel.app/424242'/> #424242 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 10.04:1              |
| `$gray_700`           | <img valign='middle' alt='gray_700' src='https://readme-swatches.vercel.app/616161'/> #616161 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 06.19:1              |
| `$gray_600`           | <img valign='middle' alt='gray_600' src='https://readme-swatches.vercel.app/757575'/> #757575 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 04.06:1              |
| `$gray_500`           | <img valign='middle' alt='gray_500' src='https://readme-swatches.vercel.app/9E9E9E'/> #9E9E9E | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 07.83:1              |
| `$gray_400`           | <img valign='middle' alt='gray_400' src='https://readme-swatches.vercel.app/BDBDBD'/> #BDBDBD | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 11.17:1              |
| `$gray_300`           | <img valign='middle' alt='gray_300' src='https://readme-swatches.vercel.app/E0E0E0'/> #E0E0E0 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 15.09:1              |
| `$gray_200`           | <img valign='middle' alt='gray_200' src='https://readme-swatches.vercel.app/EEEEEE'/> #EEEEEE | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 18.09:1              |
| `$gray_100`           | <img valign='middle' alt='gray_100' src='https://readme-swatches.vercel.app/F5F5F5'/> #F5F5F5 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 19.26:1              |
| `$gray_050`           | <img valign='middle' alt='gray_050' src='https://readme-swatches.vercel.app/FAFAFA'/> #FAFAFA | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 20.11:1              |
| `$gray_A10`           | <img valign='middle' alt='gray_A10' src='https://readme-swatches.vercel.app/E9E9E9'/> #E9E9E9 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 17.29:1              |


### Red

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$red_900`            | `#C00000`               | `$white`             | 06.47:1              |
| `$red_800`            | `#CE1A12`               | `$white`             | 05.55:1              |
| `$red_700`            | `#DB231B`               | `$white`             | 04.92:1              |
| `$red_600`            | `#ED3020`               | `$black`             | 05.04:1              |
| `$red_500`            | `#FB3C1E`               | `$black`             | 05.76:1              |
| `$red_400`            | `#F74D40`               | `$black`             | 06.09:1              |
| `$red_300`            | `#EE6F68`               | `$black`             | 07.01:1              |
| `$red_200`            | `#F69892`               | `$black`             | 09.82:1              |
| `$red_100`            | `#FFCCCE`               | `$black`             | 14.78:1              |
| `$red_050`            | `#FFEAED`               | `$black`             | 18.24:1              |
| `$red_A10`            | `#FFF7F8`               | `$black`             | 19.91:1              |

### Pink

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$pink_900`           | `#880E4F`               | `$white`             | 09.44:1              |
| `$pink_800`           | `#AD1457`               | `$white`             | 06.96:1              |
| `$pink_700`           | `#C2185B`               | `$white`             | 05.87:1              |
| `$pink_600`           | `#D81B60`               | `$white`             | 04.94:1              |
| `$pink_500`           | `#E91E63`               | `$black`             | 04.86:1              |
| `$pink_400`           | `#EC407A`               | `$black`             | 05.58:1              |
| `$pink_300`           | `#F06292`               | `$black`             | 06.86:1              |
| `$pink_200`           | `#F48FB1`               | `$black`             | 09.41:1              |
| `$pink_100`           | `#F8BBD0`               | `$black`             | 13.01:1              |
| `$pink_050`           | `#FCE4EC`               | `$black`             | 17.47:1              |
| `$pink_A10`           | `#FDEFF4`               | `$black`             | 18.82:1              |

### Purple

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$purple_900`         | `#4A148C`               | `$white`             | 11.86:1              |
| `$purple_800`         | `#6A1B9A`               | `$white`             | 09.39:1              |
| `$purple_700`         | `#7B1FA2`               | `$white`             | 08.20:1              |
| `$purple_600`         | `#8E24AA`               | `$white`             | 07.03:1              |
| `$purple_500`         | `#9C27B0`               | `$white`             | 06.30:1              |
| `$purple_400`         | `#AB47BC`               | `$white`             | 04.81:1              |
| `$purple_300`         | `#BA68C8`               | `$black`             | 05.90:1              |
| `$purple_200`         | `#CE93D8`               | `$black`             | 08.78:1              |
| `$purple_100`         | `#E1BEE7`               | `$black`             | 12.72:1              |
| `$purple_050`         | `#F3E5F5`               | `$black`             | 17.33:1              |
| `$purple_A10`         | `#F8EFF9`               | `$black`             | 18.70:1              |

### Deep Purple

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$deep_purple_900`    | `#311B92`               | `$white`             | 12.33:1              |
| `$deep_purple_800`    | `#4527A0`               | `$white`             | 10.23:1              |
| `$deep_purple_700`    | `#512DA8`               | `$white`             | 09.16:1              |
| `$deep_purple_600`    | `#5E35B1`               | `$white`             | 08.01:1              |
| `$deep_purple_500`    | `#673AB7`               | `$white`             | 07.32:1              |
| `$deep_purple_400`    | `#7E57C2`               | `$white`             | 05.21:1              |
| `$deep_purple_300`    | `#9575CD`               | `$black`             | 05.70:1              |
| `$deep_purple_200`    | `#B39DDB`               | `$black`             | 08.76:1              |
| `$deep_purple_100`    | `#D1C4E9`               | `$black`             | 12.78:1              |
| `$deep_purple_050`    | `#EDE7F6`               | `$black`             | 17.36:1              |
| `$deep_purple_A10`    | `#F4F1FA`               | `$black`             | 18.80:1              |

### Indigo

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$indigo_900`         | `#1A237E`               | `$white`             | 13.24:1              |
| `$indigo_800`         | `#283593`               | `$white`             | 10.39:1              |
| `$indigo_700`         | `#303F9F`               | `$white`             | 08.98:1              |
| `$indigo_600`         | `#3949AB`               | `$white`             | 07.73:1              |
| `$indigo_500`         | `#3F51B5`               | `$white`             | 06.87:1              |
| `$indigo_400`         | `#5C6BC0`               | `$white`             | 04.86:1              |
| `$indigo_300`         | `#7986CB`               | `$black`             | 06.08:1              |
| `$indigo_200`         | `#9FA8DA`               | `$black`             | 09.08:1              |
| `$indigo_100`         | `#C5CAE9`               | `$black`             | 12.99:1              |
| `$indigo_050`         | `#E8EAF6`               | `$black`             | 17.53:1              |
| `$indigo_A10`         | `#EFF1F9`               | `$black`             | 18.62:1              |

### Blue

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$blue_900`           | `#29479E`               | `$white`             | 08.43:1              |
| `$blue_800`           | `#3165BE`               | `$white`             | 05.62:1              |
| `$blue_700`           | `#3676D0`               | `$white`             | 04.50:1              |
| `$blue_600`           | `#3C88E3`               | `$white`             | 03.60:1              |
| `$blue_500`           | `#3F96F1`               | `$white`             | 03.06:1              |
| `$blue_400`           | `#53A5F4`               | `$black`             | 08.05:1              |
| `$blue_300`           | `#6EB5F6`               | `$black`             | 09.60:1              |
| `$blue_200`           | `#96CAF9`               | `$black`             | 12.11:1              |
| `$blue_100`           | `#BEDEFB`               | `$black`             | 15.03:1              |
| `$blue_050`           | `#E4F2FD`               | `$black`             | 18.41:1              |
| `$blue_A10`           | `#F9FCFF`               | `$black`             | 20.39:1              |

### Light Blue

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$light_blue_900`     | `#01579B`               | `$white`             | 07.39:1              |
| `$light_blue_800`     | `#0277BD`               | `$white`             | 04.79:1              |
| `$light_blue_700`     | `#0288D1`               | `$black`             | 04.37:1              |
| `$light_blue_600`     | `#039BE5`               | `$black`             | 06.82:1              |
| `$light_blue_500`     | `#03A9F4`               | `$black`             | 07.98:1              |
| `$light_blue_400`     | `#29B6F6`               | `$black`             | 09.11:1              |
| `$light_blue_300`     | `#4FC3F7`               | `$black`             | 10.48:1              |
| `$light_blue_200`     | `#81D4FA`               | `$black`             | 12.73:1              |
| `$light_blue_100`     | `#B3E5FC`               | `$black`             | 15.53:1              |
| `$light_blue_050`     | `#E1F5FE`               | `$black`             | 18.69:1              |
| `$light_blue_A10`     | `#F0FAFE`               | `$black`             | 19.81:1              |

### Cyan

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$cyan_900`           | `#006064`               | `$white`             | 07.34:1              |
| `$cyan_800`           | `#00838F`               | `$black`             | 04.64:1              |
| `$cyan_700`           | `#0097A7`               | `$black`             | 05.98:1              |
| `$cyan_600`           | `#00ACC1`               | `$black`             | 07.67:1              |
| `$cyan_500`           | `#00BCD4`               | `$black`             | 09.14:1              |
| `$cyan_400`           | `#26C6DA`               | `$black`             | 10.17:1              |
| `$cyan_300`           | `#4DD0E1`               | `$black`             | 11.42:1              |
| `$cyan_200`           | `#80DEEA`               | `$black`             | 13.55:1              |
| `$cyan_100`           | `#B2EBF2`               | `$black`             | 16.05:1              |
| `$cyan_050`           | `#E0F7FA`               | `$black`             | 18.85:1              |
| `$cyan_A10`           | `#EFFBFC`               | `$black`             | 19.87:1              |

### Teal

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$teal_900`           | `#004D40`               | `$white`             | 09.83:1              |
| `$teal_800`           | `#00695C`               | `$white`             | 06.61:1              |
| `$teal_700`           | `#00796B`               | `$white`             | 05.32:1              |
| `$teal_600`           | `#00897B`               | `$black`             | 04.86:1              |
| `$teal_500`           | `#009688`               | `$black`             | 05.71:1              |
| `$teal_400`           | `#26A69A`               | `$black`             | 00.07:1              |
| `$teal_300`           | `#4DB6AC`               | `$black`             | 08.06:1              |
| `$teal_200`           | `#80CBC4`               | `$black`             | 11.25:1              |
| `$teal_100`           | `#B2DFDB`               | `$black`             | 14.47:1              |
| `$teal_050`           | `#E0F2F1`               | `$black`             | 18.14:1              |
| `$teal_A10`           | `#EFF8F8`               | `$black`             | 19.45:1              |

### Green

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$green_900`          | `#006216`               | `$white`             | 07.61:1              |
| `$green_800`          | `#00812B`               | `$white`             | 05.02:1              |
| `$green_700`          | `#149236`               | `$black`             | 05.19:1              |
| `$green_600`          | `#23A441`               | `$black`             | 06.45:1              |
| `$green_500`          | `#009688`               | `$black`             | 07.66:1              |
| `$green_400`          | `#53BF66`               | `$black`             | 09.01:1              |
| `$green_300`          | `#74CB82`               | `$black`             | 10.06:1              |
| `$green_200`          | `#9DD9A6`               | `$black`             | 12.09:1              |
| `$green_100`          | `#C4E8C8`               | `$black`             | 15.72:1              |
| `$green_050`          | `#E0F2F1`               | `$black`             | 18.72:1              |
| `$green_A10`          | `#F7FCF8`               | `$black`             | 20.23:1              |

### Light Green

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$light_green_900`    | `#33691E`               | `$white`             | 06.06:1              |
| `$light_green_800`    | `#558B2F`               | `$black`             | 05.12:1              |
| `$light_green_700`    | `#689F38`               | `$black`             | 06.06:1              |
| `$light_green_600`    | `#7CB342`               | `$black`             | 08.38:1              |
| `$light_green_500`    | `#8BC34A`               | `$black`             | 00.10:1              |
| `$light_green_400`    | `#9CCC65`               | `$black`             | 11.23:1              |
| `$light_green_300`    | `#AED581`               | `$black`             | 12.63:1              |
| `$light_green_200`    | `#C5E1A5`               | `$black`             | 14.68:1              |
| `$light_green_100`    | `#DCEDC8`               | `$black`             | 16.99:1              |
| `$light_green_050`    | `#F1F8E9`               | `$black`             | 19.34:1              |
| `$light_green_A10`    | `#F7FBF2`               | `$black`             | 20.03:1              |

### Lime

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$lime_900`           | `#827717`               | `$black`             | 04.06:1              |
| `$lime_800`           | `#9E9D24`               | `$black`             | 07.03:1              |
| `$lime_700`           | `#AFB42B`               | `$black`             | 09.38:1              |
| `$lime_600`           | `#C0CA33`               | `$black`             | 11.73:1              |
| `$lime_500`           | `#CDDC39`               | `$black`             | 13.89:1              |
| `$lime_400`           | `#D4E157`               | `$black`             | 14.07:1              |
| `$lime_300`           | `#DCE775`               | `$black`             | 15.73:1              |
| `$lime_200`           | `#E6EE9C`               | `$black`             | 17.07:1              |
| `$lime_100`           | `#F0F4C3`               | `$black`             | 18.43:1              |
| `$lime_050`           | `#F9FBE7`               | `$black`             | 19.98:1              |
| `$lime_A10`           | `#FCFDF3`               | `$black`             | 20.48:1              |

### Yellow

| Token name            | Background              | Foreground           | WCAG Ratio           |
| :-------------------- | :---------------------- | :------------------- | :-------------------- 
| `$yellow_900`         | `#F57F17`               | `$black`             | 07.93:1              |
| `$yellow_800`         | `#F9A825`               | `$black`             | 10.65:1              |
| `$yellow_700`         | `#FBC02D`               | `$black`             | 12.67:1              |
| `$yellow_600`         | `#FDD835`               | `$black`             | 15.05:1              |
| `$yellow_500`         | `#FFEB3B`               | `$black`             | 17.19:1              |
| `$yellow_400`         | `#FFEE58`               | `$black`             | 17.62:1              |
| `$yellow_300`         | `#FFF176`               | `$black`             | 18.09:1              |
| `$yellow_200`         | `#FFF59D`               | `$black`             | 18.79:1              |
| `$yellow_100`         | `#FFF9C4`               | `$black`             | 19.59:1              |
| `$yellow_050`         | `#FFFDE7`               | `$black`             | 20.45:1              |
| `$yellow_A10`         | `#FFFEEF`               | `$black`             | 20.67:1              |

### Amber

| Token name            | Background                                                                                     | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :--------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$amber_900`          | <img valign='middle' alt='amber_900' src='https://readme-swatches.vercel.app/FF6600'/> #FF6600 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 07.15:1              |
| `$amber_800`          | <img valign='middle' alt='amber_800' src='https://readme-swatches.vercel.app/FF8700'/> #FF8700 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 08.71:1              |
| `$amber_700`          | <img valign='middle' alt='amber_700' src='https://readme-swatches.vercel.app/FF9900'/> #FF9900 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 09.08:1              |
| `$amber_600`          | <img valign='middle' alt='amber_600' src='https://readme-swatches.vercel.app/FFAC00'/> #FFAC00 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 11.15:1              |
| `$amber_500`          | <img valign='middle' alt='amber_500' src='https://readme-swatches.vercel.app/FFBA00'/> #FFBA00 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 12.27:1              |
| `$amber_400`          | <img valign='middle' alt='amber_400' src='https://readme-swatches.vercel.app/FFC41F'/> #FFC41F | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 13.16:1              |
| `$amber_300`          | <img valign='middle' alt='amber_300' src='https://readme-swatches.vercel.app/FFD04A'/> #FFD04A | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 14.37:1              |
| `$amber_200`          | <img valign='middle' alt='amber_200' src='https://readme-swatches.vercel.app/FFDC7E'/> #FFDC7E | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 15.79:1              |
| `$amber_100`          | <img valign='middle' alt='amber_100' src='https://readme-swatches.vercel.app/FFEAB1'/> #FFEAB1 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 17.65:1              |
| `$amber_050`          | <img valign='middle' alt='amber_050' src='https://readme-swatches.vercel.app/FFF7E0'/> #FFF7E0 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 19.63:1              |
| `$amber_A10`          | <img valign='middle' alt='amber_A10' src='https://readme-swatches.vercel.app/FFFDF7'/> #FFFDF7 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 20.64:1              |

### Orange

| Token name            | Background                                                                                      | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :---------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$orange_900`         | <img valign='middle' alt='orange_900' src='https://readme-swatches.vercel.app/BF360C'/> #E65100 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 05.54:1              |
| `$orange_800`         | <img valign='middle' alt='orange_800' src='https://readme-swatches.vercel.app/EF6C00'/> #EF6C00 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.81:1              |
| `$orange_700`         | <img valign='middle' alt='orange_700' src='https://readme-swatches.vercel.app/F57C00'/> #F57C00 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.81:1              |
| `$orange_600`         | <img valign='middle' alt='orange_600' src='https://readme-swatches.vercel.app/FB8C00'/> #FB8C00 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 08.85:1              |
| `$orange_500`         | <img valign='middle' alt='orange_500' src='https://readme-swatches.vercel.app/FF9800'/> #FF9800 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 09.74:1              |
| `$orange_400`         | <img valign='middle' alt='orange_400' src='https://readme-swatches.vercel.app/FFA726'/> #FFA726 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 10.08:1              |
| `$orange_300`         | <img valign='middle' alt='orange_300' src='https://readme-swatches.vercel.app/FFB74D'/> #FFB74D | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 12.13:1              |
| `$orange_200`         | <img valign='middle' alt='orange_200' src='https://readme-swatches.vercel.app/FFCC80'/> #FFCC80 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 14.02:1              |
| `$orange_100`         | <img valign='middle' alt='orange_100' src='https://readme-swatches.vercel.app/FFE0B2'/> #FFE0B2 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 16.55:1              |
| `$orange_050`         | <img valign='middle' alt='orange_050' src='https://readme-swatches.vercel.app/FFF3E0'/> #FFF3E0 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 19.41:1              |
| `$orange_A10`         | <img valign='middle' alt='orange_A10' src='https://readme-swatches.vercel.app/FFF9EF'/> #FFF9EF | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 20.04:1              |


### Deep Orange

| Token name            | Background                                                                                           | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :--------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$deep_orange_900`    | <img valign='middle' alt='deep_orange_900' src='https://readme-swatches.vercel.app/BF360C'/> #BF360C | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 05.06:1              |
| `$deep_orange_800`    | <img valign='middle' alt='deep_orange_800' src='https://readme-swatches.vercel.app/D84315'/> #D84315 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 04.73:1              |
| `$deep_orange_700`    | <img valign='middle' alt='deep_orange_700' src='https://readme-swatches.vercel.app/E64A19'/> #E64A19 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 05.35:1              |
| `$deep_orange_600`    | <img valign='middle' alt='deep_orange_600' src='https://readme-swatches.vercel.app/F4511E'/> #F4511E | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.04:1              |
| `$deep_orange_500`    | <img valign='middle' alt='deep_orange_500' src='https://readme-swatches.vercel.app/FF5722'/> #FF5722 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.63:1              |
| `$deep_orange_400`    | <img valign='middle' alt='deep_orange_400' src='https://readme-swatches.vercel.app/FF7043'/> #FF7043 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 07.65:1              |
| `$deep_orange_300`    | <img valign='middle' alt='deep_orange_300' src='https://readme-swatches.vercel.app/FF8A65'/> #FF8A65 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 09.07:1              |
| `$deep_orange_200`    | <img valign='middle' alt='deep_orange_200' src='https://readme-swatches.vercel.app/FFAB91'/> #FFAB91 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 11.48:1              |
| `$deep_orange_100`    | <img valign='middle' alt='deep_orange_100' src='https://readme-swatches.vercel.app/FFCCBC'/> #FFCCBC | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 14.61:1              |
| `$deep_orange_050`    | <img valign='middle' alt='deep_orange_050' src='https://readme-swatches.vercel.app/FBE9E7'/> #FBE9E7 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 17.91:1              |
| `$deep_orange_A10`    | <img valign='middle' alt='deep_orange_A10' src='https://readme-swatches.vercel.app/FDF0EF'/> #FDF0EF | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 18.88:1              |

### Slate

| Token name            | Background                                                                                     | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :--------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$slate_900`          | <img valign='middle' alt='slate_900' src='https://readme-swatches.vercel.app/37434B'/> #37434B | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 10.16:1              |
| `$slate_800`          | <img valign='middle' alt='slate_800' src='https://readme-swatches.vercel.app/495864'/> #495864 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 07.33:1              |
| `$slate_700`          | <img valign='middle' alt='slate_700' src='https://readme-swatches.vercel.app/586C7A'/> #586C7A | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 05.46:1              |
| `$slate_600`          | <img valign='middle' alt='slate_600' src='https://readme-swatches.vercel.app/698191'/> #698191 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 04.07:1              |
| `$slate_500`          | <img valign='middle' alt='slate_500' src='https://readme-swatches.vercel.app/9E9E9E'/> #9E9E9E | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.53:1              |
| `$slate_400`          | <img valign='middle' alt='slate_400' src='https://readme-swatches.vercel.app/8BA2B2'/> #8BA2B2 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 07.09:1              |
| `$slate_300`          | <img valign='middle' alt='slate_300' src='https://readme-swatches.vercel.app/A1B4C2'/> #A1B4C2 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 09.82:1              |
| `$slate_200`          | <img valign='middle' alt='slate_200' src='https://readme-swatches.vercel.app/BCCAD4'/> #BCCAD4 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 12.53:1              |
| `$slate_100`          | <img valign='middle' alt='slate_100' src='https://readme-swatches.vercel.app/D5DFE6'/> #D5DFE6 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 15.52:1              |
| `$slate_050`          | <img valign='middle' alt='slate_050' src='https://readme-swatches.vercel.app/EEF2F6'/> #EEF2F6 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 18.66:1              |
| `$slate_A10`          | <img valign='middle' alt='slate_A10' src='https://readme-swatches.vercel.app/EBECED'/> #EBECED | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 17.75:1              |

### Brown

| Token name            | Background                                                                                     | Foreground                                                                                | WCAG Ratio           |
| :-------------------- | :--------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | -------------------: | 
| `$brown_900`          | <img valign='middle' alt='brown_900' src='https://readme-swatches.vercel.app/3E2723'/> #3E2723 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/FFFFFF'/> $white | 13.82:1              |
| `$brown_800`          | <img valign='middle' alt='brown_800' src='https://readme-swatches.vercel.app/4E342E'/> #4E342E | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 11.32:1              |
| `$brown_700`          | <img valign='middle' alt='brown_700' src='https://readme-swatches.vercel.app/5D4037'/> #5D4037 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 09.31:1              |
| `$brown_600`          | <img valign='middle' alt='brown_600' src='https://readme-swatches.vercel.app/6D4C41'/> #6D4C41 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 07.06:1              |
| `$brown_500`          | <img valign='middle' alt='brown_500' src='https://readme-swatches.vercel.app/795548'/> #795548 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 06.55:1              |
| `$brown_400`          | <img valign='middle' alt='brown_400' src='https://readme-swatches.vercel.app/8D6E63'/> #8D6E63 | <img valign='middle' alt='white' src='https://readme-swatches.vercel.app/000000'/> $white | 04.62:1              |
| `$brown_300`          | <img valign='middle' alt='brown_300' src='https://readme-swatches.vercel.app/A1887F'/> #A1887F | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 06.34:1              |
| `$brown_200`          | <img valign='middle' alt='brown_200' src='https://readme-swatches.vercel.app/BCAAA4'/> #BCAAA4 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 09.42:1              |
| `$brown_100`          | <img valign='middle' alt='brown_100' src='https://readme-swatches.vercel.app/D7CCC8'/> #D7CCC8 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 13.36:1              |
| `$brown_050`          | <img valign='middle' alt='brown_050' src='https://readme-swatches.vercel.app/EFEBE9'/> #EFEBE9 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 17.73:1              |
| `$brown_A10`          | <img valign='middle' alt='brown_A10' src='https://readme-swatches.vercel.app/F4F1F0'/> #F4F1F0 | <img valign='middle' alt='black' src='https://readme-swatches.vercel.app/000000'/> $black | 18.68:1              |




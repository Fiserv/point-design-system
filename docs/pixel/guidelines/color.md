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

## Pixel's core color token architecture

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
| `$interative`                   | '$blue_800'           | '$blue_600'            |
| `$highlight`                    |                       |                        |
| `$overlay`                      | 'rgba($black,.50)'    | 'rgba($black,.50)'     |
| `$skeleton_element`             | '$gray_400'           | '$gray_800'            |
| `$skeleton_background`          | '$gray_200'           | 'gray_900'             |


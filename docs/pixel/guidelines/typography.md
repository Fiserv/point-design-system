# Typography

Our approach to the typographic system uses Fiserv approved **Open Sans** as its default typeface. It has been carefully engineered with suitable scales, styles, and weights to help create clear hierarchies and organize information that guides users through Fiserv products or experiences.

## Fiserv approved fonts

| Property           | Desktop/tablet     | iOS phone          | Android phone      | Alternate          |
| :----------------- | :----------------- | :----------------- | :----------------- | :----------------- |
| Font               | **Segoe UI**       | **San Francisco**  | **Roboto**         | **Open Sans**      |
| Font Weight        | **Regular**        | **Regular**        | **Regular**        | **Regular**        |
| Font Size          | **14px/16px**      | **16px**           | **16px**           | **14px/16px**      |

## Type tokens and sets
Type tokens are pre-set configurations of typographic elements such as font size, weight, or leading (line height) that are specifically calibrated for use alongside components and product patterns. Selecting the appropriate type style is determined by layout or template structure. Layouts may have several levels of architecture or areas that require varying typographic hierarchies.

## Type scale

The Pixel design system's type scale is built on a single equation. The formula for our scale was created to provide hierarchy for all types of experiences. The formula assumes that y₀=12px.

## Pixel's typography token architecture

### Base tokens

| Token name          | Font               | Weight             | Size         | Line height  |
| :------------------ | :----------------- | :----------------- | :----------- | :----------- | 
| `base_font`         | **Open Sans**      |                    |              |              |
| `base_font_light`   |                    | 300 light          |              |              |
| `base_font_regular` |                    | 400 regular        |              |              |
| `base_font_bold`    |                    | 700 bold           |              |              |



### Body
There are two body styles for standard and compact moments. Standard styles have a suffix of `_standard` and compact styles have a suffix of `_compact`.

- **Standard** - With a slightly taller line height than `body_compact`, this body style is used in productive layouts for long paragraphs with more than four lines. Use also for longer body copy in components such as accordion or contained list. It is always left-aligned.
- **Compact** - This is for short paragraphs with no more than four lines and is commonly used in components.

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$body_1_standard_light`   | `$base_font`       | `$base_font_light`   | 14px         | 20px         |
| `$body_1_standard_regular` | `$base_font`       | `$base_font_regular` | 14px         | 20px         |
| `$body_1_standard_bold`    | `$base_font`       | `$base_font_bold`    | 14px         | 20px         |
| `$body_1_compact_light`    | `$base_font`       | `$base_font_light`   | 14px         | 16px         |
| `$body_1_compact_regular`  | `$base_font`       | `$base_font_regular` | 14px         | 16px         |
| `$body_1_compact_bold`     | `$base_font`       | `$base_font_bold`    | 14px         | 16px         |
| `$body_2_standard_light`   | `$base_font`       | `$base_font_light`   | 16px         | 24px         |
| `$body_2_standard_regular` | `$base_font`       | `$base_font_regular` | 16px         | 24px         |
| `$body_2_standard_bold`    | `$base_font`       | `$base_font_bold`    | 16px         | 24px         |
| `$body_2_compact_light`    | `$base_font`       | `$base_font_light`   | 16px         | 20px         |
| `$body_2_compact_regular`  | `$base_font`       | `$base_font_regular` | 16px         | 20px         |
| `$body_2_compact_bold`     | `$base_font`       | `$base_font_bold`    | 16px         | 20px         |

### Button

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$button_1_light`          | `$base_font`       | `$base_font_light`   | 14px         | 16px         |
| `$button_1_regular`        | `$base_font`       | `$base_font_regular` | 14px         | 16px         |
| `$button_1_bold`           | `$base_font`       | `$base_font_bold`    | 14px         | 16px         |
| `$button_2_light`          | `$base_font`       | `$base_font_light`   | 16px         | 20px         |
| `$button_2_regular`        | `$base_font`       | `$base_font_regular` | 16px         | 20px         |
| `$button_2_bold`           | `$base_font`       | `$base_font_bold`    | 16px         | 20px         |

### Label

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$label_1_light`           | `$base_font`       | `$base_font_light`   | 14px         | 18px         |
| `$label_1_regular`         | `$base_font`       | `$base_font_regular` | 14px         | 18px         |
| `$label_1_bold`            | `$base_font`       | `$base_font_bold`    | 14px         | 18px         |
| `$label_2_light`           | `$base_font`       | `$base_font_light`   | 16px         | 20px         |
| `$label_2_regular`         | `$base_font`       | `$base_font_regular` | 16px         | 20px         |
| `$label_2_bold`            | `$base_font`       | `$base_font_bold`    | 16px         | 20px         |

### Helper Text

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$helper_text_1_light`     | `$base_font`       | `$base_font_light`   | 12px         | 16px         |
| `$helper_text_1_regular`   | `$base_font`       | `$base_font_regular` | 12px         | 16px         |
| `$helper_text_1_bold`      | `$base_font`       | `$base_font_bold`    | 12px         | 16px         |
| `$helper_text_2_light`     | `$base_font`       | `$base_font_light`   | 14px         | 20px         |
| `$helper_text_2_regular`   | `$base_font`       | `$base_font_regular` | 14px         | 20px         |
| `$helper_text_2_bold`      | `$base_font`       | `$base_font_bold`    | 14px         | 20px         |

### Code

This is for code snippets and code elements.

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :------------------- | :----------- | :----------- | 
| `$code_1_regular`          | Courier            | `$base_font_regular` | 12px         | 16px         |
| `$code_1_bold`             | Courier            | `$base_font_bold`    | 12px         | 16px         |
| `$code_2_regular`          | Courier            | `$base_font_regular` | 14px         | 20px         |
| `$code_2_bold`             | Courier            | `$base_font_bold`    | 14px         | 20px         |
| `$code_3_regular`          | Courier            | `$base_font_regular` | 16px         | 24px         |
| `$code_3_bold`             | Courier            | `$base_font_bold`    | 16px         | 24px         |

### Legal

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$legal_1_light`           | `$base_font`       | `$base_font_light`   | 12px         | 16px         |
| `$legal_1_regular`         | `$base_font`       | `$base_font_regular` | 12px         | 16px         |
| `$legal_2_bold`            | `$base_font`       | `$base_font_bold`    | 14px         | 18px         |
| `$legal_2_light`           | `$base_font`       | `$base_font_light`   | 14px         | 18px         |
| `$legal_3_regular`         | `$base_font`       | `$base_font_regular` | 16px         | 20px         |
| `$legal_3_bold`            | `$base_font`       | `$base_font_bold`    | 16px         | 20px         |


### Heading 1 (H1)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h1_standard_light`       | `$base_font`       | `$base_font_light`   | 42px         | 50px         |
| `$h1_standard_regular`     | `$base_font`       | `$base_font_regular` | 42px         | 50px         |
| `$h1_standard_bold`        | `$base_font`       | `$base_font_bold`    | 42px         | 50px         |
| `$h1_compact_light`        | `$base_font`       | `$base_font_light`   | 42px         | 46px         |
| `$h1_compact_regular`      | `$base_font`       | `$base_font_regular` | 42px         | 46px         |
| `$h1_compact_bold`         | `$base_font`       | `$base_font_bold`    | 42px         | 46px         |

### Heading 2 (H2)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h2_standard_light`       | `$base_font`       | `$base_font_light`   | 34px         | 40px         |
| `$h2_standard_regular`     | `$base_font`       | `$base_font_regular` | 34px         | 40px         |
| `$h2_standard_bold`        | `$base_font`       | `$base_font_bold`    | 34px         | 40px         |
| `$h2_compact_light`        | `$base_font`       | `$base_font_light`   | 34px         | 38px         |
| `$h2_compact_regular`      | `$base_font`       | `$base_font_regular` | 34px         | 38px         |
| `$h2_compact_bold`         | `$base_font`       | `$base_font_bold`    | 34px         | 38px         |

### Heading 3 (H3)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h3_standard_light`       | `$base_font`       | `$base_font_light`   | 28px         | 36px         |
| `$h3_standard_regular`     | `$base_font`       | `$base_font_regular` | 28px         | 36px         |
| `$h3_standard_bold`        | `$base_font`       | `$base_font_bold`    | 28px         | 36px         |
| `$h3_compact_light`        | `$base_font`       | `$base_font_light`   | 28px         | 32px         |
| `$h3_compact_regular`      | `$base_font`       | `$base_font_regular` | 28px         | 32px         |
| `$h3_compact_bold`         | `$base_font`       | `$base_font_bold`    | 28px         | 32px         |

### Heading 4 (H4)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h4_standard_light`       | `$base_font`       | `$base_font_light`   | 20px         | 28px         |
| `$h4_standard_regular`     | `$base_font`       | `$base_font_regular` | 20px         | 28px         |
| `$h4_standard_bold`        | `$base_font`       | `$base_font_bold`    | 20px         | 28px         |
| `$h4_compact_light`        | `$base_font`       | `$base_font_light`   | 20px         | 24px         |
| `$h4_compact_regular`      | `$base_font`       | `$base_font_regular` | 20px         | 24px         |
| `$h4_compact_bold`         | `$base_font`       | `$base_font_bold`    | 20px         | 24px         |

### Heading 5 (H5)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h5_standard_light`       | `$base_font`       | `$base_font_light`   | 16px         | 24px         |
| `$h5_standard_regular`     | `$base_font`       | `$base_font_regular` | 16px         | 24px         |
| `$h5_standard_bold`        | `$base_font`       | `$base_font_bold`    | 16px         | 24px         |
| `$h5_compact_light`        | `$base_font`       | `$base_font_light`   | 16px         | 22px         |
| `$h5_compact_regular`      | `$base_font`       | `$base_font_regular` | 16px         | 22px         |
| `$h5_compact_bold`         | `$base_font`       | `$base_font_bold`    | 16px         | 22px         |

### Heading 6 (H6)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h6_standard_light`       | `$base_font`       | `$base_font_light`   | 14px         | 20px         |
| `$h6_standard_regular`     | `$base_font`       | `$base_font_regular` | 14px         | 20px         |
| `$h6_standard_bold`        | `$base_font`       | `$base_font_bold`    | 14px         | 20px         |
| `$h6_compact_light`        | `$base_font`       | `$base_font_light`   | 14px         | 18px         |
| `$h6_compact_regular`      | `$base_font`       | `$base_font_regular` | 14px         | 18px         |
| `$h6_compact_bold`         | `$base_font`       | `$base_font_bold`    | 14px         | 18px         |

### Heading 7 (H7)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h7_standard_light`       | `$base_font`       | `$base_font_light`   | 12px         | 18px         |
| `$h7_standard_regular`     | `$base_font`       | `$base_font_regular` | 12px         | 18px         |
| `$h7_standard_bold`        | `$base_font`       | `$base_font_bold`    | 12px         | 18px         |
| `$h7_compact_light`        | `$base_font`       | `$base_font_light`   | 12px         | 16px         |
| `$h7_compact_regular`      | `$base_font`       | `$base_font_regular` | 12px         | 16px         |
| `$h7_compact_bold`         | `$base_font`       | `$base_font_bold`    | 12px         | 16px         |

### Heading 8 (H8)

| Token name                 | Font               | Weight               | Size         | Line height  |
| :------------------------- | :----------------- | :-----------------   | :----------- | :----------- | 
| `$h8_standard_light`       | `$base_font`       | `$base_font_light`   | 10px         | 16px         |
| `$h8_standard_regular`     | `$base_font`       | `$base_font_regular` | 10px         | 16px         |
| `$h8_standard_bold`        | `$base_font`       | `$base_font_bold`    | 10px         | 16px         |
| `$h8_compact_light`        | `$base_font`       | `$base_font_light`   | 10px         | 12px         |
| `$h8_compact_regular`      | `$base_font`       | `$base_font_regular` | 10px         | 12px         |
| `$h8_compact_bold`         | `$base_font`       | `$base_font_bold`    | 10px         | 12px         |



# Size and spacing

The sizing tokens help you control the proportions of your system’s components at the atom level for global consistency. There can impact height, weight, padding, and margin. Depending on the components defined in your initial system, the maturity of this template can include any additional components or attributes in the future.

The tokens should function as a common language during the product cycle. It is critical that the naming convention should be agreed upon between both development and design. Some tokens values can remain empty, using the token as a placeholder for other themes.

>[!Note]
> If you are looking for tokens related to component colors, please reference the [color guidelines](color.md) for the Pixel design system.

## Component specifications

### Base models

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$base_small`                   | 32px                  | 32px                  |
| `$base_medium`                  | 40px                  | 40px                  |
| `$base_large`                   | 48px                  | 48px                  |
| `$base_padding`                 | `$spacing_16`         | `$spacing_16`         |
| `$base_margin`                  | `$spacing_8`          | `$spacing_8`          |
| `$base_border`                  | `$border_01`          | `$border_01`          |
| `$base_border_radius`           | 4px                   | 4px                   |

### Accordion

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$accordion_small`              | (min-height:40px)     | (min-height:40px)     |
| `$accordion_medium`             | (min-height:48px)     | (min-height:48px)     |
| `$accordion_large`              | (min-height:56px)     | (min-height:56px)     |
| `$accordion_padding`            | `$base_padding`       | `$base_padding`       |
| `$accordion_margin`             | `$base_margin`        | `$base_margin`        |
| `$accordion_border`             | `$base_border`        | `$base_border`        |
| `$accordion_border_radius`      |                       |                       |

### Avatar

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$avatar_x_small`               | 28px                  | 28px                  |
| `$avatar_small`                 | 38px                  | 38px                  |
| `$avatar_medium`                | 48px                  | 48px                  |
| `$avatar_large`                 | 58px                  | 58px                  |
| `$avatar_x_large`               | 68px                  | 68px                  |
| `$avatar_xx_large`              | 88px                  | 88px                  |
| `$avatar_padding`               |                       |                       |
| `$avatar_margin`                |                       |                       |
| `$avatar_border`                | `$border_02`          | `$border_02`          |
| `$avatar_border_radius`         | 100px                 | 100px                 |

### Badge

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$badge_small`                  | 12px                  | 12px                  |
| `$badge_medium`                 | 18px                  | 18px                  |
| `$badge_large`                  | 28px                  | 28px                  |
| `$badge_padding`                |                       |                       |
| `$badge_margin`                 |                       |                       |
| `$badge_border`                 | `$border_01`          | `$border_01`          |
| `$badge_border_radius`          | 50px                  | 50px                  |

### Bottom Navigation

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$bottom_nav_small`             |                       |                       |
| `$bottom_nav_medium`            |                       |                       |
| `$bottom_nav_large`             |                       |                       |
| `$bottom_nav_padding`           | `$spacing_8`          | `$spacing_8`          |
| `$bottom_nav_margin`            | `$spacing_4`          | `$spacing_4`          |
| `$bottom_nav_border`            | `$border_01`          | `$border_01`          |
| `$bottom_nav_border_radius`     | 10px                  | 10px                  |

### Breadcrumb

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$breadcrumb_small`             |                       |                       |
| `$breadcrumb_medium`            |                       |                       |
| `$breadcrumb_large`             |                       |                       |
| `$breadcrumb_padding`           | `$base_padding`       | `$base_padding`       |
| `$breadcrumb_margin`            | `$based_margin`       | `$base_margin`        |
| `$breadcrumb_border`            | `$border_01`          | `$border_01`          |
| `$breadcrumb_border_radius`     |                       |                       |

### Button

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$button_small`                 | `$base_small`         | `$base_small`         |
| `$button_medium`                | `$base_medium`        | `$base_medium`        |
| `$button_large`                 | `$base_large`         | `$base_large`         |
| `$button_padding`               | `$base_padding`       | `$base_padding`       |
| `$button_margin`                | `$base_margin`        | `$base_margin`        |
| `$button_border`                | `$base_border`        | `$base_border`        |
| `$button_border_radius`         | `$base_border_radius` | `$base_border_radius` |

### Button Group

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$button_group_small`           | `$base_small`         | `$base_small`         |
| `$button_group_medium`          | `$base_medium`        | `$base_medium`        |
| `$button_group_large`           | `$base_large`         | `$base_large`         |
| `$button_group_padding`         | `$base_padding`       | `$base_padding`       |
| `$button_group_margin`          | `$base_margin`        | `$base_margin`        |
| `$button_group_border`          | `$base_border`        | `$base_border`        |
| `$button_group_border_radius`   | `$base_border_radius` | `$base_border_radius` |

### Card

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$card_small`                   |                       |                       |
| `$card_medium`                  |                       |                       |
| `$card_large`                   |                       |                       |
| `$card_padding`                 | `$base_padding`       | `$base_padding`       |
| `$card_margin`                  | `$base_margin`        | `$base_margin`        |
| `$card_border`                  | `$base_border`        | `$base_border`        |
| `$card_border_radius`           | `$base_border_radius` | `$base_border_radius` |

#### Card Footer

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$card_footer_small`            | (min-height:40px)     | (min-height:40px)     |
| `$card_footer_medium`           | (min-height:48px)     | (min-height:48px)     |
| `$card_footer_large`            | (min-height:56px)     | (min-height:56px)     |
| `$card_footer_padding`          | `$base_padding`       | `$base_padding`       |
| `$card_footer_margin`           | `$base_margin`        | `$base_margin`        |
| `$card_footer_border`           | `$base_border`        | `$base_border`        |
| `$card_footer_border_radius`    |                       |                       |

#### Card Header

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$card_header_small`            | (min-height:40px)     | (min-height:40px)     |
| `$card_header_medium`           | (min-height:48px)     | (min-height:48px)     |
| `$card_header_large`            | (min-height:56px)     | (min-height:56px)     |
| `$card_header_padding`          | `$base_padding`       | `$base_padding`       |
| `$card_header_margin`           | `$base_margin`        | `$base_margin`        |
| `$card_header_border`           | `$base_border`        | `$base_border`        |
| `$card_header_border_radius`    |                       |                       |


### Checkbox

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$checkbox_small`               | 24px                  | 24px                  |
| `$checkbox_medium`              |                       |                       |
| `$checkbox_large`               |                       |                       |
| `$checkbox_padding`             | `$base_padding`       | `$base_padding`       |
| `$checkbox_margin`              | `$base_margin`        | `$base_margin`        |
| `$checkbox_border`              | `$border_01`          | `$border_01`          |
| `$checkbox_border_radius`       | `$base_border_radius` | `$base_border_radius` |

### Date Input

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$date_picker_small`            | `$base_small`         | `$base_small`         |
| `$date_picker_medium`           | `$base_medium`        | `$base_medium`        |
| `$date_picker_large`            | `$base_large`         | `$base_large`         |
| `$date_picker_padding`          | `$base_padding`       | `$base_padding`       |
| `$date_picker_margin`           | `$base_margin`        | `$base_margin`        |
| `$date_picker_border`           | `$base_border`        | `$base_border`        |
| `$date_picker_border_radius`    | `$base_border_radius` | `$base_border_radius` |

### Dropdown

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$dropdown_small`               | `$base_small`         | `$base_small`         |
| `$dropdown_medium`              | `$base_medium`        | `$base_medium`        |
| `$dropdown_large`               | `$base_large`         | `$base_large`         |
| `$dropdown_padding`             | `$base_padding`       | `$base_padding`       |
| `$dropdown_margin`              | `$base_margin`        | `$base_margin`        |
| `$dropdown_border`              | `$base_border`        | `$base_border`        |
| `$dropdown_border_radius`       | `$base_border_radius` | `$base_border_radius` |

### File Input

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$file_input_small`             | `$base_small`         | `$base_small`         |
| `$file_input_medium`            | `$base_medium`        | `$base_medium`        |
| `$file_input_large`             | `$base_large`         | `$base_large`         |
| `$file_input_padding`           | `$base_padding`       | `$base_padding`       |
| `$file_input_margin`            | `$base_margin`        | `$base_margin`        |
| `$file_input_border`            | `$base_border`        | `$base_border`        |
| `$file_input_border_radius`     | `$base_border_radius` | `$base_border_radius` |

### Header

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$header_small`                 | (min-height:40px)     | (min-height:40px)     |
| `$header_medium`                | (min-height:48px)     | (min-height:48px)     |
| `$header_large`                 | (min-height:56px)     | (min-height:56px)     |
| `$header_padding`               | `$base_padding`       | `$base_padding`       |
| `$header_margin`                | `$base_margin`        | `$base_margin`        |
| `$header_border`                | `$border_01`          | `$border_01`          |
| `$header_border_radius`         |                       |                       |

### Icon

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$icon_small`                   | 20px                  | 20px                  |
| `$icon_medium`                  | 24px                  | 24px                  |
| `$icon_large`                   | 28px                  | 28px                  |
| `$icon_padding`                 |                       |                       |
| `$icon_margin`                  |                       |                       |
| `$icon_border`                  |                       |                       |
| `$icon_border_radius`           |                       |                       |

### Loader

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$loader_small`                 |                       |                       |
| `$loader_medium`                |                       |                       |
| `$loader_large`                 |                       |                       |
| `$loader_padding`               |                       |                       |
| `$loader_margin`                | `$base_margin`        | `$base_margin`        |
| `$loader_border`                |                       |                       |
| `$loader_border_radius`         | 100%                  | 100%                  |

### Notification

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$notificaiton_small`           |                       |                       |
| `$notificaiton_medium`          |                       |                       |
| `$notificaiton_large`           |                       |                       |
| `$notificaiton_padding`         | `$base_padding`       | `$base_padding`       |
| `$notificaiton_margin`          | `$base_margin`        | `$base_margin`        |
| `$notificaiton_border`          | `$border_01`          | `$border_01`          |
| `$notificaiton_border_radius`   | `$base_border_radius` | `$base_border_radius` |

### Pagination

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$pagination_small`             | (min-height:40px)     | (min-height:40px)     |
| `$pagination_medium`            | (min-height:48px)     | (min-height:48px)     |
| `$pagination_large`             | (min-height:56px)     | (min-height:56px)     |
| `$pagination_padding`           | `$base_padding`       | `$base_padding`       |
| `$pagination_margin`            | `$base_margin`        | `$base_margin`        |
| `$pagination_border`            | `$border_01`          | `$border_01`          |
| `$pagination_border_radius`     |                       |                       |

### Password Input

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$password_input_small`         | `$base_small`         | `$base_small`         |
| `$password_input_medium`        | `$base_medium`        | `$base_medium`        |
| `$password_input_large`         | `$base_large`         | `$base_large`         |
| `$password_input_padding`       | `$base_padding`       | `$base_padding`       |
| `$password_input_margin`        | `$base_margin`        | `$base_margin`        |
| `$password_input_border`        | `$base_border`        | `$base_border`        |
| `$password_input_border_radius` | `$base_border_radius` | `$base_border_radius` |

### Phone Input

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$phone_input_small`            | `$base_small`         | `$base_small`         |
| `$phone_input_medium`           | `$base_medium`        | `$base_medium`        |
| `$phone_input_large`            | `$base_large`         | `$base_large`         |
| `$phone_input_padding`          | `$base_padding`       | `$base_padding`       |
| `$phone_input_margin`           | `$base_margin`        | `$base_margin`        |
| `$phone_input_border`           | `$base_border`        | `$base_border`        |
| `$phone_input_border_radius`    | `$base_border_radius` | `$base_border_radius` |

### Progress Indicator

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$progress_small`               |                       |                       |
| `$progress_medium`              |                       |                       |
| `$progress_large`               |                       |                       |
| `$progress_padding`             | `$base_padding`       | `$base_padding`       |
| `$progress_margin`              | `$base_margin`        | `$base_margin`        |
| `$progress_border`              | `$border_01`          | `$border_01`          |
| `$progress_border_radius`       | `$base_border_radius` | `$base_border_radius` |

### Radio Button

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$radio_small`                  | 24px                  | 24px                  |
| `$radio_medium`                 |                       |                       |
| `$radio_large`                  |                       |                       |
| `$radio_padding`                | `$base_padding`       | `$base_padding`       |
| `$radio_margin`                 | `$base_margin`        | `$base_margin`        |
| `$radio_border`                 | `$border_01`          | `$border_01`          |
| `$radio_border_radius`          | 100%                  | 100%                  |

### Search Input

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$search_input_small`           | `$base_small`         | `$base_small`         |
| `$search_input_medium`          | `$base_medium`        | `$base_medium`        |
| `$search_input_large`           | `$base_large`         | `$base_large`         |
| `$search_input_padding`         | `$base_padding`       | `$base_padding`       |
| `$search_input_margin`          | `$base_margin`        | `$base_margin`        |
| `$search_input_border`          | `$base_border`        | `$base_border`        |
| `$search_input_border_radius`   | `$base_border_radius` | `$base_border_radius` |

### Stepper

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$stepper_small`                | `$base_small`         | `$base_small`         |
| `$stepper_medium`               | `$base_medium`        | `$base_medium`        |
| `$stepper_large`                | `$base_large`         | `$base_large`         |
| `$stepper_padding`              | `$base_padding`       | `$base_padding`       |
| `$stepper_margin`               | `$base_margin`        | `$base_margin`        |
| `$stepper_border`               | `$base_border`        | `$base_border`        |
| `$stepper_border_radius`        | `$base_border_radius` | `$base_border_radius` |

### Table

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$table_small`                  | (min-height:40px)     | (min-height:40px)     |
| `$table_medium`                 | (min-height:48px)     | (min-height:48px)     |
| `$table_large`                  | (min-height:56px)     | (min-height:56px)     |
| `$table_padding`                | `$base_padding`       | `$base_padding`       |
| `$table_margin`                 | `$base_margin`        | `$base_margin`        |
| `$table_border`                 | `$border_01`          | `$border_01`          |
| `$table_border_radius`          |                       |                       |

### Tab Navigation

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$tab_small`                    | `$base_small`         | `$base_small`         |
| `$tab_medium`                   | `$base_medium`        | `$base_medium`        |
| `$tab_large`                    | `$base_large`         | `$base_large`         |
| `$tab_padding`                  | `$base_padding`       | `$base_padding`       |
| `$tab_margin`                   | `$base_margin`        | `$base_margin`        |
| `$tab_border`                   | `$base_border`        | `$base_border`        |
| `$tab_border_radius`            | `$base_border_radius` | `$base_border_radius` |

### Tag

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$tag_x_small`                  | 18px                  | 18px                  |
| `$tag_small`                    | 22px                  | 22px                  |
| `$tag_medium`                   | 28px                  | 28px                  |
| `$tag_large`                    | 32px                  | 38px                  |
| `$tag_x_large`                  | 40px                  | 40px                  |
| `$tag_padding`                  |                       |                       |
| `$tag_margin`                   | `$base_margin`        | `$base_margin`        |
| `$tag_border`                   | `$border_01`          | `$border_01`          |
| `$tag_border_radius`            | 100px                 | 100px                 |

### Textarea

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$textarea_small`               |                       |                       |
| `$textarea_medium`              |                       |                       |
| `$textarea_large`               |                       |                       |
| `$textarea_padding`             | `$base_padding`       | `$base_padding`       |
| `$textarea_margin`              | `$base_margin`        | `$base_margin`        |
| `$textarea_border`              | `$border_01`          | `$border_01`          |
| `$textarea_border_radius`       | `$base_border_radius` | `$base_border_radius` |

### Toggle Switch

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$toggle_small`                 |                       |                       |
| `$toggle_medium`                |                       |                       |
| `$toggle_large`                 |                       |                       |
| `$toggle_padding`               | `$base_padding`       | `$base_padding`       |
| `$toggle_margin`                | `$base_margin`        | `$base_margin`        |
| `$toggle_border`                | `$border_01`          | `$border_01`          |
| `$toggle_border_radius`         | `$base_border_radius` | `$base_border_radius` |

### Tooltip

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$tooltip_small`                |                       |                       |
| `$tooltip_medium`               |                       |                       |
| `$tooltip_large`                |                       |                       |
| `$tooltip_padding`              | `$base_padding`       | `$base_padding`       |
| `$tooltip_margin`               | `$base_margin`        | `$base_margin`        |
| `$tooltip_border`               |                       |                       |
| `$tooltip_border_radius`        | `$base_border_radius` | `$base_border_radius` |

## Borders

The border tokens help you control the proportions of your system’s components at the atom level for global consistency. This is a supplemental token structure for other tokens. Depending on the components defined in your initial system, the maturity of this template can include any additional components or attributes in the future.

The tokens should function as a common language during the product cycle. It is critical that the naming convention should be agreed upon between both development and design. Some tokens values can remain empty, using the token as a placeholder for other themes.

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$border_01`                    | 01px                  | 01px                  |
| `$border_02`                    | 02px                  | 02px                  |
| `$border_03`                    | 03px                  | 03px                  |
| `$border_04`                    | 04px                  | 04px                  |
| `$border_05`                    | 05px                  | 05px                  |
| `$border_06`                    | 06px                  | 06px                  |
| `$border_07`                    | 07px                  | 07px                  |
| `$border_08`                    | 08px                  | 08px                  |
| `$border_09`                    | 09px                  | 09px                  |
| `$border_10`                    | 10px                  | 10px                  |

## Spacing

The spacing tokens help you control the proportions of your system’s components at the atom level for global consistency. This is a supplemental token structure for other tokens. Depending on the components defined in your initial system, the maturity of this template can include any additional components or attributes in the future.

The tokens should function as a common language during the product cycle. It is critical that the naming convention should be agreed upon between both development and design. Some tokens values can remain empty, using the token as a placeholder for other themes.

| Token name                      | Light theme           | Dark theme            |
| :------------------------------ | :-------------------- | :-------------------- |
| `$spacing_01`                   | 01px                  | 01px                  |
| `$spacing_02`                   | 02px                  | 02px                  |
| `$spacing_03`                   | 03px                  | 03px                  |
| `$spacing_04`                   | 04px                  | 04px                  |
| `$spacing_05`                   | 05px                  | 05px                  |
| `$spacing_06`                   | 06px                  | 06px                  |
| `$spacing_07`                   | 07px                  | 07px                  |
| `$spacing_08`                   | 08px                  | 08px                  |
| `$spacing_09`                   | 09px                  | 09px                  |
| `$spacing_10`                   | 10px                  | 10px                  |
| `$spacing_11`                   | 11px                  | 11px                  |
| `$spacing_12`                   | 12px                  | 12px                  |
| `$spacing_13`                   | 13px                  | 13px                  |
| `$spacing_14`                   | 14px                  | 14px                  |
| `$spacing_15`                   | 15px                  | 15px                  |
| `$spacing_16`                   | 16px                  | 16px                  |
| `$spacing_17`                   | 17px                  | 17px                  |
| `$spacing_18`                   | 18px                  | 18px                  |
| `$spacing_19`                   | 19px                  | 19px                  |
| `$spacing_20`                   | 20px                  | 20px                  |
| `$spacing_21`                   | 21px                  | 21px                  |
| `$spacing_22`                   | 22px                  | 22px                  |
| `$spacing_23`                   | 23px                  | 23px                  |
| `$spacing_24`                   | 24px                  | 24px                  |
| `$spacing_25`                   | 25px                  | 25px                  |
| `$spacing_26`                   | 26px                  | 26px                  |
| `$spacing_27`                   | 27px                  | 27px                  |
| `$spacing_28`                   | 28px                  | 28px                  |
| `$spacing_29`                   | 29px                  | 29px                  |
| `$spacing_30`                   | 30px                  | 30px                  |
| `$spacing_32`                   | 32px                  | 32px                  |
| `$spacing_34`                   | 34px                  | 34px                  |
| `$spacing_36`                   | 36px                  | 36px                  |
| `$spacing_38`                   | 38px                  | 38px                  |
| `$spacing_40`                   | 40px                  | 40px                  |

## Box Shadow

| Token name                      | Color            | Length 1 | Length 2  | Length 3 |
| :------------------------------ | :--------------- | : ------ | : ------- | :------- |
| `$shadow_1`                     | rgba(0,0,0,0.12) | 0px      | 01px      | 03px     |
|                                 | rgba(0,0,0,0.24) | 0px      | 01px      | 02px     |
| `$shadow_2`                     | rgba(0,0,0,0.16) | 0px      | 03px      | 06px     |
|                                 | rgba(0,0,0,0.23) | 0px      | 03px      | 06px     |
| `$shadow_3`                     | rgba(0,0,0,0.19) | 0px      | 10px      | 20px     |
|                                 | rgba(0,0,0,0.23) | 0px      | 06px      | 06px     |
| `$shadow_4`                     | rgba(0,0,0,0.25) | 0px      | 14px      | 28px     |
|                                 | rgba(0,0,0,0.22) | 0px      | 10px      | 10px     |
| `$shadow_5`                     | rgba(0,0,0,0.25) | 0px      | 14px      | 28px     |
|                                 | rgba(0,0,0,0.22) | 0px      | 10px      | 10px     |









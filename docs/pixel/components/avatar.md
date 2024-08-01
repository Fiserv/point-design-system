# Avatar

An avatar is a visual representation of a person across products. It is typically a photo, an illustration, the initials of the user's first and last name, or an icon. Avatars are used to support personalization and to convey the online status of the user.

## Usage

### When to use

Use an avatar to provide user identification, profile personalization, or customization. An avatar can also be used to provide information about a user's online status. It may include a merchant or a business logo for quick and easy brand recognition. Always use an avatar with a user's name or a business name.

### Cover fit

The size of the image is scaled up to completely cover the control area. As a result, parts of the image may be outside the shape. Use the Cover fit type if the focal point is in the center of the image.

### Contained fit

The image is scaled down to fit into the control area. The entire image is displayed but might not fully fill the shape. In this case, the control displays a default background color. The image itself is always centered inside the shape. Use the Contain fit type for the product pictures that need to be displayed in full.

### Variants

An avatar is a visual representation of a user in the digital space. Usually, an avatar displays the user in one of the following ways:

- A user's photo.
- The user’s initials.
- A placeholder icon instead of the user’s personal data (photo or initials).

Always display avatars in a circle. This ensures that all users are represented equally on the user interface.

| Variant     | Purpose                                                                    |
| :---------- | :------------------------------------------------------------------------- |
| Initials    | Initials can be used as the default if an image' is not used.              |
| Images      | Avatar displays a selected or predetermined image of the user or business. |
| Placeholder | Placeholder images are used for both initials and images.                  |

### Initials

The initials stand for the first name and last name of a person - for example JD for Jane Doe. The name that comes first depends on the language-specific settings.

Initials can have up to two alphabetical characters (A-Z, a-z). If more that, two initials are required for longer names (such as Anna Maria Agusti Suarez), the gender-neutral placeholder icon is displayed instead.

Some languages don’t build on an alphabet, or don’t use initials at all. In some cases, the gender-neutral person icon is displayed instead.

### Images

Business images display a product, company, object, logo, or other business-related content.

### Placeholder

Placeholder images are used for both avatar and business images when no other image is available.

- The default placeholder for an avatar is a gender-neutral person icon inside a circle.
- The default placeholder for a business image is a neutral product icon inside a square.
- You can specify your own default placeholder icon for business images. Always replace the default product icon if there is a more suitable icon for your scenario and industry.

### Badge (PIP)

- If an avatar is clickable, you can show an optional badge and icon.
- Use a badge to indicate that the avatar is interactive.
- Use an icon to indicate the action triggered by clicking the avatar.
- Use an image to show relationship.

This feature gives users visual affordance of the available action and is particularly useful for images. To ensure that the image and the badge icon are properly displayed, don’t use the badge for any avatar sizes less than “Small”.
When you use a badge and icon, always provide a corresponding tooltip for your avatar to indicate the action.

## Style

Below is the token architecture color build of the components. The token can be changed or defined through the token mapping script that has been placed in the application repository.

### Color

| Color                      | Element                    | Property                   | Token name                 |
| :------------------------- | :------------------------- | :------------------------- | :------------------------- |
| Black                      | Container                  | Background Color           | `$gray_900`                |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| White                      | Container                  | Background Color           | `$white`                   |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Gray                       | Container                  | Background Color           | `$gray_500`                |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| Light gray                 | Container                  | Background Color           | `$gray_200`                |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Blue                       | Container                  | Background Color           | `$blue_800`                |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| Light blue                 | Container                  | Background Color           | `$blue_100`                |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Slate                      | Container                  | Background Color           | `$slate_400`               |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| Light slate                | Container                  | Background Color           | `$slate_100`               |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Red                        | Container                  | Background Color           | `$red_900`                 |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| Light red                  | Container                  | Background Color           | `$red_100`                 |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Green                      | Container                  | Background Color           | `$green_800`               |
|                            | Text                       | Text Color                 | `$text_on_color`           |
|                            | Icon                       | SVG Color                  | `$icon_on_color`           |
| Light green                | Container                  | Background Color           | `$green_100`               |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Yellow                     | Container                  | Background Color           | `$orange_100`              |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |
| Light yellow               | Container                  | Background Color           | `$orange_100`              |
|                            | Text                       | Text Color                 | `$text_primary`            |
|                            | Icon                       | SVG Color                  | `$icon_primary`            |

### Typography

| Size                  | Element                | Font size | Font weight             | Token name                 |
| :-------------------- | :--------------------  | :-------- | :---------------------- | :------------------------- | 
| XX-large              | Text                   | 42px      | 400 Regular             | `$h1_compact_regular`      |
|                       | Link                   | 20px      | 400 Regular             | `$h4_compact_regular`      |
| X-large               | Text                   | 34px      | 400 Regular             | `$h2_compact_regular`      |
|                       | Link                   | 16px      | 400 Regular             | `$h5_compact_regular`      |
| Large                 | Text                   | 28px      | 400 Regular             | `$h3_compact_regular`      |
|                       | Link                   | 16px      | 400 Regular             | `$h5_compact_regular`      |
| Medium                | Text                   | 42px      | 400 Regular             | `$h5_compact_regular`      |
|                       | Link                   | 20px      | 400 Regular             | `$h4_compact_regular`      |
| Small                 | Text                   | 16px      | 400 Regular             | `$h5_compact_regular`      |
|                       | Link                   | 14px      | 400 Regular             | `$h6_compact_regular`      |
| X-small               | Text                   | 14px      | 400 Regular             | `$h6_compact_regular`      |
|                       | Link                   | 14px      | 400 Regular             | `$h6_compact_regular`      |

### Token Architecture

| Token name                 | Description                                            |
| :------------------------- | :----------------------------------------------------- |
| `$avatar_xx_large`         | Defines height for the **xx-large** variant.           |
| `$avatar_x_large`          | Defines height for the **x-large** variant.            |
| `$avatar_large`            | Defines height for the **large** variant.              |
| `$avatar_medium`           | Defines height for the **medium** variant.             |
| `$avatar_small`            | Defines height for the **small** variant.              |
| `$avatar_x_small`          | Defines height for the **x-small** variant.            |
| `$avatar_padding`          | Defines **padding** for the component.                 |
| `$avatar_margin`           | Defines **margin** for the component.                  |
| `$avatar_border`           | Defines **border** weight for the accordion component. |
| `$avatar_border_radius`    | Defines **border radius** for the component.           |

### Structure

| Size                 | Element               | Property                | Size      | Token name                  |
| :--------------------| :-------------------- | :---------------------- | :-------- | :-------------------------- |
| XX-large             | Container             | Height x Width          | 88px      | `$avatar_xx_large`          |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 24px      |                             |
| X-large              | Container             | Height x Width          | 68px      | `$avatar_x_large`           |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 24px      |                             |
| Large                | Container             | Height x Width          | 58px      | `$avatar_large`             |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 24px      |                             |
| Medium               | Container             | Height x Width          | 48px      | `$avatar_medium`            |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 24px      |                             |
| Small                | Container             | Height x Width          | 38px      | `$avatar_small`             |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 20px      |                             |
| X-small              | Container             | Height x Width          | 28px      | `$avatar_x_small`           |
|                      | Badge (PIP)           | Height x Width          | 28px      |                             |
|                      |                       | Box Shadow              |           | `$shadow_2`                 |
|                      | Icon                  | Height x Width          | 16px      |                             |
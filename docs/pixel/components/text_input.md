# Text Input

Text inputs enable users to enter free-form text data. The type of text field used should reflect the length of the content you expect the user to enter. The default text input is for short, one-line content, whereas text area is for longer, multi-line entries.

## Usage

### When to use

 - A user needs to input unique information that cannot be predicted with a preset of options.
 - A user needs to input memorable data that can be entered more quickly in a free-hand format versus a more complex control.

### When not to use

If a user can only enter an option from a predefined list, then avoid using a free-form text input as it is likely to result in an error. Consider using a selection control such as a dropdown, select, or radio button group instead.

### Variants

| Variant    | Purpose |
|:---------- | :------ |
| Text Input | When the expected user input is a single line of text, as opposed to a paragraph. |
| Text Area  | When the expected user input is more than one sentence. |

### Anatomy

1. **Label** - Text that informs the user about the content they need to enter in the field. It is required unless you get an approved accessibility exemption.
2. **Field** - The container in which a user enters data. Must meet 3:1 non-text contrast requirement.
3. **Helper Text (optional)** - Assistive text that can provide additional aid or context to the user. Often used to explain the correct data format.
4. **Value** - The content the user has entered the field.
5. **Resize handle (textarea only)** - Allows a user to manipulate the field height by making it longer or shorter.
6. **Character counter (textarea only)** - Indicate the number of characters being entered and the total number of characters allowed.

### Formats

Use a text input when the expected user input is a single line of text. Text inputs have a fixed height and are used as a simple free-form data entry. Users can enter any combination of letters, numbers, or symbols. The text input can be formatted to accept various types of formats.

| Format     | Description                                                                    | Example           |
|:---------- | :----------------------------------------------------------------------------- | :---------------- |
| Text Input | The value is formatted to input a date pattern.                                | `12/03/2029 `     |
| Tel        | The value is formatted to input a phone number.                                | `(403) 555-8493 ` |
| Password   | The value is formatted to input a maskable password.                           | `****** `         |
| Email      | The value is formatted to input an email address based on domain.              | `user@domain.com` |
| File       | Used for uploading a file.                                                     |                   | 
| Search     | Used to search an application, table or defined section.                       |                   | 
| Number     | The value is formatted with deceasing/increasing numerical controls. (Stepper) |                   |
| URL        | The value is formatting to input an URL.                                       |                   |

### Password

Password input is a sub-variant of text input. It is used to collect private data and will hide the characters as a user enters them. A user can choose to toggle on the character visibility by clicking the view icon on the far right of the input field. When using a password input be sure to provide detailed helper text listing any requirements related to the data format, such as types of characters allowed or date structure.

### Masked input data

Like the password variant above, this provides real time masking of sensitive data with the option of providing fully masked, or partially mask.

### Currency data

Using this variant for the text input provides better user intention within the form structure. The dollar sign is auto generated based on user input of numerical data. If the users input alphabetical data, the text input will generate an error validation.

### Textarea

Use a text area when the expected user input is more than a few words and could span multiple lines. It is commonly used for features like user commentary or descriptions. It supports all the same states and functionality as text input except for the password functionality. Text area has several unique functionalities not included in the default text input, like the resize handle and character counter.

#### Resize handle

Included by default in text area is the resize handle. It allows a user to manipulate the field height by making it longer or shorter. The resize handle has no effect on the width of the text area container, it only effects the height. If the user makes the field size shorter than the content inside the field, then a vertical scroll will become available.

#### Character counter

A character counter can be added to text area to indicate both the number of characters being entered and the total number of characters allowed. Once the max number of characters is reached the text area should prevent the user from entering any additional character and provide messaging to the user that a limit has been met.

#### Textarea height

Textarea has a variable height that can be lengthened or shortened by the user using the resize handle in the bottom right of the field. By default, textarea has a minimum height of 40px/2.5rem but no maximum height.

#### Text input and textarea width

The field widths of both text input and text area should reflect the intended length of the content while still aligning to the grid columns or mini unit grid. Unlike the height, the width of the text area cannot be controlled by the user. There are no minimum or maximum widths, but you should avoid excessively wide fields that are disproportionate to the intended data being collected.

 - Do make text input widths proportional to the content and align to grid columns.
 - Do not make text inputs excessively wide just to fill in space.

### Alignment

Labels and field containers should vertically align to the grid and with other form components on a page.

### Content

#### Labels

Effective labeling helps users understand what information to enter a text input. Text fields should always have a label. There are rare instances where the context of an input negates the need for a visible label, but we advise you consult an accessibility expert before proceeding with a label-less design.

- Use sentence-style capitalization for all labels, except for product names and proper nouns.
- Keep the label short and concise.
- Labels should clearly state the requirement status.
- Do not use colons after label names.

#### Helper text

Optional helper text is pertinent information that assists the user in correctly completing a field. It is often used to explain the correct data format.

- Use sentence-style capitalization, and in most cases, write the text as full sentences with punctuation.
- Helper text is an optional feature and can be used in place of a tooltip.
- When used, helper text is always available when the input is focused and appears underneath the field. The exceptions are when an error or warning message replaces the helper text.

#### Placeholder text

Optional placeholder text provides hints or examples of what to enter. Placeholder text disappears after the user begins entering data into the input and should not contain crucial information.

- Use sentence-style capitalization, and in most cases, write the text as a direct statement without punctuation.
- Placeholder text is not required and by default not shown in text input fields.
- Placeholder text can be harmful to user interactions and should only be added when necessary.

### Overflow content

#### Overflow in a text input

If a user’s content is unexpectedly too long for the single line of a text input, then the value content can horizontally scroll inside the field container when moving the cursor from one end of the value to the other.

#### Overflow in a textarea

If a user’s content exceeds the vertical space of the variable textarea then a user can either expand the field container using the resize handle or they can vertically scroll the content inside the set field container.

### Validation

An error state is triggered if the data is invalid, or a required field is left empty. Error states have three visual indicators to signify invalid content: a red border, an error icon indicator, and an error message.

### Default values

Where possible, add programmatic assistance. Detect and pre-fill inputs to reduce errors and save time. When the software can’t determine the value that belongs in an input, use type-ahead to make suggestions. Use sentence-case for default values, detected values, and auto-completion text.

### Required versus optional

Text inputs can be labeled as either optional or required depending on the depending on the circumstance.

### Universal behaviors

#### Mouse

Users can activate a text input by clicking on the field container. A separate click is required to activate any additional actions associated with the text input such as a tooltip or password visibility toggle.

#### Keyboard

For additional keyboard interactions, see the accessibility tab.

| Keystroke                           | Interaction                                                                           |
|:----------------------------------- | :------------------------------------------------------------------------------------ |
| `Tab`                               | Brings focus to the text input.                                                       |
| `Enter` or `Space`                  | Opens any associated actions added to the input, such as a password visibility toggle.|
| `Ctrl` of `Opt` + Left/Right arrows | Moves you word by word inside the field.                                              |
| `Ctrl` or `Opt` + Up/Down arrows    | Relocates you to the start or end of the input content.                               |

## Style

Below is the token architecture color build of the components. The token can be changed or defined through the token mapping script that has been placed in the application repository.

### Color

**Text Input**

| State                      | Element                    | Property                   | Token name                 |
| :------------------------- | :------------------------- | :------------------------- | :------------------------- |
| Enabled                    | Container                  | Background Color           | `$field_1`                 |
|                            |                            | Border Color               | `$border_strong_1`         | 
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_secondary`          |
|                            | Icon                       | SVG Color                  | `$icon_secondary`          |
| Focus                      | Container                  | Background Color           | `$focus_highlight`         |
|                            |                            | Border Color               | `$focus`                   |  
|                            |                            | Box Shadow                 | `$shadow_1`                | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_secondary`          |
|                            | Icon                       | SVG Color                  | `$icon_secondary`          |
| Disabled                   | Container                  | Background Color           | `$field_disabled_1`        |
|                            |                            | Border Color               | `$border_disabled_1`       |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_disabled`           |
|                            | Value                      | Text Color                 | `$text_disabled`           |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_disabled`           |
|                            | Icon                       | SVG Color                  | `$icon_disabled`           |
| Error                      | Container                  | Background Color           | `$support_bg_error`        |
|                            |                            | Border Color               | `$support_error`           |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$support_error`           |
|                            | Value                      | Text Color                 | `$support_error`           |
|                            | Placeholder                | Text Color                 | `$support_error`           |
|                            | Help Text                  | Text Color                 | `$support_error`           |
|                            | Icon                       | SVG Color                  | `$support_error`           |
| Success                    | Container                  | Background Color           | `$support_bg_success`      |
|                            |                            | Border Color               | `$support_success`         |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$support_success`         |
|                            | Value                      | Text Color                 | `$support_success`         |
|                            | Placeholder                | Text Color                 | `$support_success`         |
|                            | Help Text                  | Text Color                 | `$support_success`         |
|                            | Icon                       | SVG Color                  | `$support_success`         |

**Textarea**

| State                      | Element                    | Property                   | Token name                 |
| :------------------------- | :------------------------- | :------------------------- | :------------------------- |
| Enabled                    | Container                  | Background Color           | `$field_1`                 |
|                            |                            | Border Color               | `$border_strong_1`         |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_secondary`          |
|                            | Icon                       | SVG Color                  | `$icon_secondary`          |
|                            | Resize handle              | SVG Color                  | `$icon_secondary`          |
|                            | Character counter          | Text Color                 | `$icon_secondary`          |
| Focus                      | Container                  | Background Color           | `$focus_highlight`         |
|                            |                            | Border Color               | `$focus`                   |  
|                            |                            | Box Shadow                 | `$shadow_1`                | 
|                            | Label                      | Text Color                 | `$text_secondary`          |
|                            | Value                      | Text Color                 | `$text_primary`            |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_secondary`          |
|                            | Icon                       | SVG Color                  | `$icon_secondary`          |
|                            | Resize handle              | SVG Color                  | `$focus`                   |
|                            | Character counter          | Text Color                 | `$focus`                   |
| Disabled                   | Container                  | Background Color           | `$field_disabled_1`        |
|                            |                            | Border Color               | `$border_disabled_1`       |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$text_disabled`           |
|                            | Value                      | Text Color                 | `$text_disabled`           |
|                            | Placeholder                | Text Color                 | `$text_placeholder`        |
|                            | Help Text                  | Text Color                 | `$text_disabled`           |
|                            | Icon                       | SVG Color                  | `$icon_disabled`           |
|                            | Resize handle              | SVG Color                  | `$icon_disabled`           |
|                            | Character counter          | Text Color                 | `$text_disabled`           |
| Error                      | Container                  | Background Color           | `$support_bg_error`        |
|                            |                            | Border Color               | `$support_error`           |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$support_error`           |
|                            | Value                      | Text Color                 | `$support_error`           |
|                            | Placeholder                | Text Color                 | `$support_error`           |
|                            | Help Text                  | Text Color                 | `$support_error`           |
|                            | Icon                       | SVG Color                  | `$support_error`           |
|                            | Resize handle              | SVG Color                  | `$support_error`           |
|                            | Character counter          | Text Color                 | `$support_error`           |
| Success                    | Container                  | Background Color           | `$support_bg_success`      |
|                            |                            | Border Color               | `$support_success`         |  
|                            |                            | Box Shadow                 |                            | 
|                            | Label                      | Text Color                 | `$support_success`         |
|                            | Value                      | Text Color                 | `$support_success`         |
|                            | Placeholder                | Text Color                 | `$support_success`         |
|                            | Help Text                  | Text Color                 | `$support_success`         |
|                            | Icon                       | SVG Color                  | `$support_success`         |
|                            | Resize handle              | SVG Color                  | `$support_success`         |
|                            | Character counter          | Text Color                 | `$support_success`         |

### Typography

Text input labels and placeholder text should be set in sentence case, with only the first word in a phrase and any proper nouns capitalized. Text input labels should be three words or less.

| State      | Element         | Font size | Font weight | Token name                |
| ---------- | --------------- | --------- | ----------- | ------------------------- | 
| Small      | Label           | 14px      | 700 bold    | `$label_1_bold`           |
|            | Helper Text     | 12px      | 400 regular | `$helper_text_1_regular`  |
|            | Value           | 14px      | 400 regular | `$body_1_compact_regular` |
|            | Placeholder     | 14px      | 400 regular | `$body_1_compact_regular` |
|            | Contextual Menu | 14px      | 400 regular | `$body_1_compact_regular` |
| Medium     | Label           | 14px      | 700 bold    | `$label_1_bold`           |
|            | Helper Text     | 12px      | 400 regular | `$helper_text_1_regular`  |
|            | Value           | 14px      | 400 regular | `$body_1_compact_regular` |
|            | Placeholder     | 14px      | 400 regular | `$body_1_compact_regular` |
|            | Contextual Menu | 14px      | 400 regular | `$body_1_compact_regular` |
| Large      | Label           | 14px      | 700 bold    | `$label_1_bold`           |
|            | Helper Text     | 12px      | 400 regular | `$helper_text_1_regular`  |
|            | Value           | 16px      | 400 regular | `$body_2_compact_regular` |
|            | Placeholder     | 16px      | 400 regular | `$body_2_compact_regular` |
|            | Contextual Menu | 16px      | 400 regular | `$body_2_compact_regular` |

### Token Architecture

| Token name                  | Description                                            |
| :-------------------------- | :----------------------------------------------------- |
| `$text_input_small`         | Defines height for the **small** variant.              |
| `$text_input_medium`        | Defines height for the **medium** variant.             |
| `$text_input_large`         | Defines height for the **large** variant.              |
| `$text_input_padding`       | Defines **padding** for the component.                 |
| `$text_input_margin`        | Defines **margin** for the component.                  |
| `$text_input_border`        | Defines **border** weight for the accordion component. |
| `$text_input_border_radius` | Defines **border radius** for the component.           |

### Structure

**Text Input**

| Element               | Property                | Size      | Token name                  |
| :-------------------- | :---------------------- | :-------- | :-------------------------- |
| Input                 | Padding Right x Left    | 16px      | `$phone_input_padding`      |
|                       | Border                  | 1px       | `$phone_input_border`       |
|                       | Border Radius           | 4px       | `$phone_input_border_radius`|
| Icon (Left)           | Margin Right            | 8px       | `$phone_input_margin`       |
| Icon (Right)          | Margin Left             | 8px       | `$phone_input_margin`       |
| Label                 | Margin Bottom           | 2px       | `$spacing_2`                |
| Helper Text           | Margin Top              | 2px       | `$spacing_2`                |

**Textarea**

| Element               | Property                | Size      | Token name                  |
| :-------------------- | :---------------------- | :-------- | :-------------------------- |
| Input                 | Padding Right x Left    | 16px      | `$phone_input_padding`      |
|                       | Border                  | 1px       | `$phone_input_border`       |
|                       | Border Radius           | 4px       | `$phone_input_border_radius`|
| Icon (Left)           | Margin Right            | 8px       | `$phone_input_margin`       |
| Icon (Right)          | Margin Left             | 8px       | `$phone_input_margin`       |
| Label                 | Margin Bottom           | 2px       | `$spacing_2`                |
| Helper Text           | Margin Top              | 2px       | `$spacing_2`                |
| Character Counter     | Margin Top              | 2px       | `$spacing_2`                |
| Resize Handle         | Height x Width          | 8px       |                             |

### Size

| Size    | Element               | Property       | Size      | Token name                |
| :------ | :-------------------- | :------------- | :-------- | :------------------------ |
| Small   | Input                 | Height         | 32px      | `$phone_input_small`      |
|         | Icon                  | Height x Width | 20px      | `$icon_small`             |
| Medium  | Input                 | Height         | 40px      | `$phone_input_medium`     |
|         | Icon                  | Height x Width | 24px      | `$icon_medium`            |
| Large   | Input                 | Height         | 48px      | `$phone_input_large`      |
|         | Icon                  | Height x Width | 28px      | `$icon_large`             |

## Accessibility

The component bakes keyboard operation into its components, improving the experience of blind users and others who operate via the keyboard. The component incorporates many other accessibility considerations, some of which are described below.

### Keyboard interaction

Text inputs and text areas replicate the default HTML component operation. Each input field is a tab stop, as are any preceding information icons (which open with Enter/Space and close with Esc). For password inputs, the component provides a keyboard-operable ability to toggle the password value’s visibility using `Enter` or `Space`.

### Labeling and helper text

The component’s programmatically surfaces both the input’s label and any helper text to assistive technologies such as screen readers. Any error messages for text inputs are also accessibly revealed.

### Development recommendations

Keep these considerations in mind if you are modifying the component or creating a custom component.

- Labels are properly associated with inputs using the for attribute.
- Helper text is surfaced to assistive technology through aria-describedby.




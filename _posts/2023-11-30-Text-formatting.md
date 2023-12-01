---
layout: post
title: "Text Formatting"
date: 2023-11-28 10:00:00 +0100
categories: guides
image: https://files.cocobut.net/screenshots/2023-11-30_18.15.24.png
---

Here's a guide to help you use text formatting features in chat.

### Color Formatting
- **Change Color**: To color text, type `<color:[color]>`. Replace `[color]` with a color name or hex code. To reset to the default color, use `<reset>` or `<r>`.
  - *Example*: `<color:red>This is red <color:#00ff00>This is green <r>Back to default`

### Text Decoration Tags
Enhance your text with decoration tags:
- **Bold (`<b>`)**: Makes text bold.
- **Italic (`<i>`)**: Italicizes text.
- **Underline (`<underline>`)**: Underlines text.
- **Strikethrough (`<st>`)**: Strikes through text.
All these tags need to be closed, to do it simply write them again and and `/` after `<`, e.g. `<b>Text</b>`.

### Gradient Text
Create text with a color gradient:
- **Basic Gradient**: Type `<gradient:[color1]:[color2]:...>` or `<gr:[color1]:[color2]:...>`. Don't forget to close the tag using `</gradient>` or `</gr>`.
- **Advanced Gradients**: Use `<hard_gradient>` or `<hgr>` for sharp transitions, `<rainbow>` or `<rb>` for rainbow effects. Don't forget to close the tag.

### Hover Text
Display text on mouse hover:
- **Usage**: Type `<hover:show_text:[value]>` or `<hover:[value]>`. `[value]` is the hover text.
  - *Example*: `<hover:Hello>Hover over me!</hover>`

### Emojis and Special Symbols
Insert emojis and symbols with ease:
- **Emoji Format**: Like in Discord, type `:[name]:`.
  - *Examples*: 
    - potion ->:test_tube:
    - item -> Shows the item youre holding
    - trident -> :trident:
    - rod ->:fishing_pole_and_fish:
    - shrug -> ¯\\_(ツ)_/¯
    - bow -> :bow_and_arrow:
    - bell ->:bell:
    - heart -> ❤
    - bucket -> :bucket:
    - sword -> :dagger:
    - shears -> ✂
    - pos -> %player:pos_x% %player:pos_y% %player:pos_z%
    - fire ->:fire:
    - table -> (╯°□°）╯︵ ┻━┻
    - skull -> ☠
- **Dynamic Symbols**: Tags like `:item:` display your held item, `:pos:` shows your coordinates.

For a full list of text formatting tags visit [this url](https://placeholders.pb4.eu/user/text-format/).

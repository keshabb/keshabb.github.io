### Update Profile
In `_config.yml`, you can modify personal info such as your *photo, phone number, email*, and other social accounts. 

```yml
profile_img: assets/img/profile.webp
icon_img: assets/img/icon.webp

name: "Your Name Here"
job: "〈Your Job Here〉"

phone_number: 012-345-6789
address: City, Country
email: email@example.com
linkedin_username: linkedin
github_username: github
...

```

### Create a Topic

All resume information should be placed in a directory named '`_data`'. You may need to manage personal data in separate groups, making a *Yaml* (`.yml`) file for each subject.

```
._data
├── SUBJECT1.yml
├── SUBJECT2.yml
├── SUBJECT3.yml
...

```

For instance,

```
._data
├── Awards.yml
├── Education.yml
├── Experience.yml
├── Languages.yml
├── Projects.yml
├── Publications.yml
├── Skills.yml
```

### Fill your infomation

Open the *Yaml* file which you created right before. Add the following materials inside of the file.

* **subject**: title of a subject
* **listing-order**: determines the display order (from top to bottom)
* **icon**: representative icon to be displayed (pick out from `resources/svgs`)
* **contents**: The details of each item, listed in `KEY`-`VALUE` pairs 

```yml
subject:
listing-order:
icon:
contents:
  - title: ITEM 1
    KEY: VALUE
    KEY: VALUE
    ...
  - title: ITEM 2
    KEY: VALUE
    ...
```

For a better understanding, see the example below.

```yml
subject: Education
listing-order: 1
icon: "/assets/img/graduation-cap.svg"
contents:
  - title: Stanfort University, MA in Computer Science
    description:
      - Development of algorithms for tracking the facial expressions
      - Optimizing parameter efficient fine tuning for fairness
    grade: "**GPA**: `4.1/4.3`"
    date: Mar. 2014 - Feb. 2016
  ...

```

The rendered output looks like this:

![example1](https://i.ibb.co/9TGKPrv/123312.webp)

See also the advanced example. 

> **Important**: You can use markdown syntax to **apply text bold, italic, and underlined** effects or **create HTML elements** (including image, links, span, etc.)!

```yml
subject: Projects
listing-order: 3
icon: "/assets/img/clipboard-list.svg"
contents:
  - title: "ChatPPT ([https://chat.opena1.com/](https://chat.openai.com/))"
    description: 
      - Chatbot developed based on a large language model
      - Designed Generative algorithm to generate novel human-like content
      - "Technology Used: Rust, Typescript, Python, Ruby"
    image: "![](https://i.ibb.co/hX2wYLB/231321.webp)"
  ...

```

![example](https://i.ibb.co/tCNCyYr/231321.webp)

## Build from Gem package

If you don't like the above setup option (clone/fork the original github repo), then you can also build your site by installing the gem package remotely. Read this altenative [guide](https://github.com/keshabb/keshabb.github.io/blob/main/docs/Installation%20from%20package.md).

## Customizing

### Change Color Palette
Wanna pick another color? You can edit the base theme palette in `assets/css/style.scss`.
```css
:root {
    --color-background: #fffdfb;
    --theme1-light: #F6D8CB;
    --theme1-medium: #D0A694;
    --theme1-dim: #B07D67;
    --theme1-dark: #8A5843;
    --theme2-light: #B1B1C2;
    ...

}
```

### Site Shortcut Icon
To replace the shortcut icon displayed on browser tab, modify *icon_img* field in `_config.yml`.
![shortcut](https://i.ibb.co/g9cYjRj/213213214.webp)

```yml
icon_img: "<IMAGE URL/PATH>"
```

## License
© 2024 *Keshab Budhathoky*. This theme is available as open source under the terms of the [MIT License](https://opensource.org/license/mit/).
# Abstract Red

As I was browsing throught the themes in HACS, I grew weary of the dull and mundane themes that were available. I created this theme to spark some life into HACS Themes. I hope you enjoy!

## Screenshots
![Main Dashboard](https://i.imgur.com/hOtmvHr.png)
![Pop up Windows](https://i.imgur.com/zcZgSbB.png)
[More Screenshots](https://imgur.com/gallery/aozDUGS)

## Installation
---

Currently, only the manual installation in available until I'm able to figure out how to add my theme into HACS.

### Prerequisites

Add the following code to your `configuration.yaml` file (reboot required).

```yaml
frontend:
  ... # your configuration.
  themes: !include_dir_merge_named themes
  ... # your configuration.
```

### Manual

Navigate to `~/config/themes` in your Home Assistant server and clone this repository with: `git clone https://github.com/python4lyfe/abstractRed`.

### Add the font
This theme requires you to add the `Comfortaa` font as a resource to your lovelace configuration:
```yaml
resources:
  - url: https://fonts.googleapis.com/css?family=Comfortaa&display=swap
  type: css
```

### Add or Change the background

You can download the background shown in the screenshots from [here](https://pxwall.com/wp-content/uploads/2018/07/Wallpaper%20Lines,%20digital,%20red,%204K,%20Abstract%20461651997.jpg) - or you can use your own!

1. Download your background image to `~/config/www/backgrounds` (you may need to create the backgrounds folder if it doesn't already exist)
2. Change the image name in the abstract_red.yaml file (Line 3)
```yaml
  background-image: "center / cover no-repeat url('/local/backgrounds/red_abstract.jpg') fixed"
```
3. Go to services and trigger the `frontend.reload_themes` service

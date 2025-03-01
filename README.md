<h3 align="center">Marzbanify Template</h3>

<p align="center">
  Simple, beautiful, and user-friendly HTML template for <a href="https://github.com/Gozargah/Marzban">Marzban</a> subscription page
  <br>
  <a href="https://denisromanov.ru/projects/marzbanify-template-demo"><strong>Live demo »</strong></a>
  <br>
  <br>
  <a href="https://github.com/dermv/marzbanify-template/tree/main#features">Features</a>
  ·
  <a href="https://github.com/dermv/marzbanify-template/tree/main#mini-version">mini Version</a>
  ·
  <a href="https://github.com/dermv/marzbanify-template/tree/main#install">Install</a>
  ·
  <a href="https://github.com/dermv/marzbanify-template/tree/main#personalization">Personalization</a>
</p>

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./.github/assets/dark.png">
    <source media="(prefers-color-scheme: light)" srcset="./.github/assets/light.png">
    <img alt="Marzbanify Template" src="./.github/assets/dark.png">
  </picture>
</p>


## Features

- Clean and intuitive design with minimal code
- System, light, and dark theme modes
- Multi-language support: English, Russian, Chinese, Persian
- Step-by-step guides for PC, Android, and iOS
- Automatic detection of user preferences: theme, language, and device


## mini Version
Pure minimalism. Just the header and step-by-step guide.
<br>
<a href="https://denisromanov.ru/projects/marzbanify-template-mini-demo">Live demo »</a>

<details>
  <summary>Preview</summary>
  <p>
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="./.github/assets/mini/dark.png">
      <source media="(prefers-color-scheme: light)" srcset="./.github/assets/mini/light.png">
      <img alt="Marzbanify Template mini" src="./.github/assets/mini/dark.png">
    </picture>
  </p>
</details>


## Install

### 1. Upload the template file to the server

Choose the version and run the corresponding command.

**Main version:**
```
sudo wget -O /var/lib/marzban/templates/subscription/index.html https://raw.githubusercontent.com/dermv/marzbanify-template/main/index.html
```

**Mini version:**
```
sudo wget -O /var/lib/marzban/templates/subscription/index.html https://raw.githubusercontent.com/dermv/marzbanify-template/main/mini/index.html
```

### 2. Configure the subscription page path

**Automatically**

Run these commands to set the path:
```
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```

**Manually**

Edit the Marzban `.env` file and add the following lines:
```
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

### 3. Restart Marzban

Apply the changes by restarting Marzban:
```
marzban restart
```

## Personalization

To personalize, edit the `index.html` file.

### Main Values

Find and replace these default values with your own.

| Name         | Value                                                                               |
|--------------|-------------------------------------------------------------------------------------|
| Description  | `Simple, beautiful, and user-friendly HTML template for Marzban subscription page.` |
| Title        | `Marzbanify Template`                                                               |
| Favicons     | `apple-touch-icon.png`, `favicon-16x16.png`, `favicon-32x32.png`                    |
| Logo         | `logo.png`                                                                          |
| Support link | `https://t.me/`                                                                     |

### Optional Variables

These variables allow further personalization.

| Variable          | Description                                                 |
|-------------------|-------------------------------------------------------------|
| `DEFAULT_THEME`   | Default website theme (`system`, `light`, `dark`)           |
| `SUB_URL_SCHEMES` | URL schemes for quick subscription import                   |
| `DEFAULT_LOCALE`  | Default locale for content display (`en`, `ru`, `zh`, `fa`) |
| `MESSAGES`        | Translation data for multi-language support                 |

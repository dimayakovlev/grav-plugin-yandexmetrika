# Grav Yandex.Metrika Plugin

`Yandex.Metrika` is a [Grav](http://github.com/getgrav/grav) plugin that can be used for adding Yandex.Metrika counter code on to website pages. The main purpose of this plugin is to allow configure counter code parameters without manual editing template.

# Installation

## Manual Installation

Download the zip version of this repository and unzip it under `/your/site/grav/user/plugins`. Then, rename the folder to `yandexmetrika`.

You should now have all the plugin files under

	/your/site/grav/user/plugins/bootstrapper

# Usage

Firstly you should register your website in [Yandex.Metrika](https://metrika.yandex.com/).

Registered website has its own counter number. Use this counter number to configure plugin.

```
enabled: false					# Enable / Disable this plugin
counter_number: 				# Counter number
webvisor: true					# Enable / Disable Webvisor option
click_map: true					# Enable / Disable Click map option
track_links: true				# Enable / Disable Track links option
accurate_track_bounce: true		# Enable / Disable Accurate track bounce option
track_hash: false				# Enable / Disable Track hash option
async_code: true				# Enable / Disable Asynchronous script option
stop_index: true				# Enable / Disable Automatic page indexing option
```

After setting all configuration paste this code in the footer of Twig template of your current website theme:

```
{% if config.plugins.yandexmetrika.enabled %}
	{% include 'yandexmetrika.html.twig' %}
{% endif %}
```
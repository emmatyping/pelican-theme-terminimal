# Terminimal theme for Pelican

This is a [Pelican](https://getpelican.com) theme based on the [zola-theme-terminimal](https://github.com/pawroman/zola-theme-terminimal) theme for [zola](https://getzola.org).

## Usage

> Note: This repo is published if others want to use it but I don't really want to support other users. If you want to use it, feel free! I will probably take patches, but I probably won't fix bugs unless they affect my blog as well.

Clone this repository:

```
git clone git@github.com:emmatyping/pelican-theme-terminimal.git terminimal
```

Install the required plugins:
```
pip install pelican-minify pelican-neighbors
```
Update your `pelicanconf.py`:

```python
THEME = 'terminimal'

MENUITEMS = (
    # You can use $BASE_URL to refer to the SITEURL
    ("Home", "$BASE_URL/index.html")
    ... # Put the titles and links to items you want at the top/menu
)

# The templates require `continue` in loops
JINJA_ENVIRONMENT = {
    'extensions': ['jinja2.ext.loopcontrols']
}

# Set the accent color (options: blue, green, orange, pink, red)
ACCENT_COLOR = 'blue'
# Set the background color (options: blue, green, orange, pink, red, dark, light)
BACKGROUND_COLOR = 'dark'

PLUGINS = [
    "pelican.plugins.neighbors",
    "pelican.plugins.minify",
]

CSS_MIN = True
```

## Features/TODOs

I wanted to port over the basic theme so I could move my blog over to Pelican. I have a few things I would like to port over or add:

 - [ ] Mastodon verification support
 - [ ] RSS feed link(s)
 - [ ] OpenGraph support
 - [ ] Toggleable/device aware dark/light theming
 - [ ] Some of the configurations from the original theme
 - [ ] Fix highlighted page logic
 - [ ] Better syntax highlighting

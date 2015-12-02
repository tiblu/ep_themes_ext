# ep_themes_ext

An Etherpad Lite plugin that allows you to load external CSS stylesheets to change the layout.

# Requirements

Requires ``aceEditorCSS`` hook patch to be merged with Etherpad - https://github.com/tiblu/etherpad-lite/commit/ad2ea924b5c039ebb8df9dd97d1f5ecaeb02fb14
Hope it makes it to Etherpad release version.

# Install

``npm install ep_themes_ext``

# Configuration

In your EP ``settings.json`` add:

```
  "ep_themes_ext": {
    "default": ["https://myhost.com/static/styles/default.css"],
    "theme1": ["https://myhost.com/static/styles/theme1.css", "https://myhost.com/static/styles/theme1_extras.css"]
  }
```

When embedding EP, use ``theme`` parameter to choose the theme. For example ``https://myetherpadinstallion.com/p/testpad?theme=theme1``. Read more about embedding Etherpad - http://etherpad.org/doc/v1.5.7/#index_embed_parameters.

**NOTES:**

* The ``default`` can be an empty array, then the plugin does nothing.
* The ``default`` theme is used when no ``theme`` embed parameter is provided. 


# Credits

* CitizenOS for funding the development - https://citizenos.com/
* Implementation inspired by https://github.com/JohnMcLear/ep_themes - if you just want color scheme changes, use that instead.
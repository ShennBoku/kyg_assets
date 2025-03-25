# 🦭 KYG Assets

**KYG Assets** is a collection of resource assets gathered from various sources, curated and combined into a single repository for easy access and use in other projects. This assets maybe will be required for my other resources.

## 🌴 Features

- Combining multiple asset resources into a single asset.
- For developers, especially for creating native ui without a framework, you can store library assets such as bootstrap and others in this folder so that you don't need to store many of the same libraries in every ui folder you create.
- You can use the PolyZone module (by [mkafrin](https://github.com/mkafrin/PolyZone)) without adding new resources.
- GTA5 Vehicle b2944 (San Andreas Mercenaries - mp2023_01)
- GTA5 Vehicle b3095 (The Chop Shop - mp2023_02)
- GTA5 Vehicle b3258 (Bottom Dollar Bounties - mp2024_01)
- Postal Code Map & Minimap by [Virus_City](https://forum.cfx.re/t/release-postal-code-map-minimap-new-improved-v1-3/147458)

## 🥥 Installation

You can ensure this resource anywhere, but if you use our other KYG resources, you must ensure kyg_assets before kyg_lib.

## 🦀 HTML Usage's
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Sample Page</title>
        <link rel="stylesheet" href="nui://kyg_assets/public/css/bootstrap.min.css">
        <link rel="stylesheet" href="nui://kyg_assets/public/css/fontawesome.min.css">
        <link rel="stylesheet" href="nui://kyg_assets/public/fonts/pack.css">
    </head>
    <body>
        <h1>Hello Shenn <i class="fas fa-user"></i>!</h1>

        <script src="nui://kyg_assets/public/js/jquery-3.6.3.min.js"></script>
    </body>
</html>
```

## 🦀 PolyZone Usage's

In order to use PolyZone in your script, you must _at least_ include PolyZone's client.lua directly in your __resource.lua or fxmanifest.lua. You can do that by using FiveM's @ syntax for importing resource files:

```lua
client_scripts {
    '@kyg_assets/module/PolyZone/client.lua',
    'your_scripts_client.lua',
}
```

This will allow you to create PolyZones in your script, but will not import other zones, such as CircleZone, BoxZone, etc. All the other zones are extra, and require their own explicit imports. Here is a `client_scripts` value that will include all the zones. Note the relative order of these imports, as the ordering is necessary! Many zones rely on each other, for example EntityZone inherits from BoxZone, and all zones inherit from PolyZone (client.lua).

```lua
client_scripts {
  '@kyg_assets/module/PolyZone/client.lua',
  '@kyg_assets/module/PolyZone/BoxZone.lua',
  '@kyg_assets/module/PolyZone/EntityZone.lua',
  '@kyg_assets/module/PolyZone/CircleZone.lua',
  '@kyg_assets/module/PolyZone/ComboZone.lua',
  'your_scripts_client.lua'
}
```

For additional information on how to use PolyZone, please take a look at the [wiki](https://github.com/mkafrin/PolyZone/wiki)

## 🦀 Map & Minimap Information

- If you want to use the map in this resource, make sure the other resource does not import the map as well.
- If you want to replace a map in this resource, you can delete the contents of the Minimap folder in the stream folder with your own map file.
- If you have already imported a map in another resource, you can delete the Minimap folder in the stream folder in this resource.

## 🏄🏻‍♀️ Dependencies

- Brain
# KYG Assets

**KYG Assets** is a collection of resource assets gathered from various sources, curated and combined into a single repository for easy access and use in other projects. This assets maybe will be required for my other resources.

## Module
You can use some of the modules below without having to add new resources.

- **RageUI**
- **PolyZone** by [mkafrin](https://github.com/mkafrin/PolyZone)

## Web Assets
You can store the assets for ui creation in the 'public' folder, then you can call them with the url 'nui://kyg_assets/public/'. Example:
- **CSS**: ```<link rel="stylesheet" href="nui://kyg_assets/public/css/bootstrap.min.css">```
- **JS**: ```<script src="nui://kyg_assets/public/js/jquery-3.6.3.min.js"></script>```

## New Gamebuild Vehicles
To be able to use vehicles in the new gta build, you can move the contents of the '! DISABLED STREAM' folder into the 'stream/GTA5 Vehicles' folder. For example if you are using gamebuild 2802 and you want to add vehicles from gamebuild 2944, you can simply move the '! DISABLED STREAM/b2944' folder into the 'stream/GTA5 Vehicles' folder then don't forget to customize the fxmanifest.lua file.
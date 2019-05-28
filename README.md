# About

**usage**: `python autopak.py [install] [deploy] [help]`

**install**: copies mods into their respective install locations, zipping them into pk4 files as needed.

**deploy**: packages mods into zip and pk4 files located in the `targets/` directory of the project.

# Mod Definition

## Specification

**game_title**: (string) Title of the game that the mod is for. Used to make console output more helpful.

**mod_title**: (string) Title of the mod. Used for console output.

**is_pk4**: (boolean) If set to true, install and deploy as a pk4. Otherwise, install and deploy for Doom 3 BFG Edition.

**sources**: (list(string)) Names of folders in the project. Mod will be assembled from the contents of these folders.

**base_path**: (string) File path to the game installation. Used for installing the mod.

**game**: (string) Folder under the base path where the mod should be installed.

**zip_name**: (string) File name to use when deploying the mod as a zip.

**pk4_name**: string) File name to use when installing or deploying the mod as a pk4.

**should_deploy**: (boolean): Whether or not the defined mod should be deployed.

## Example mods.json

```
[
    {
        "game_title": "RBDOOM 3 BFG",
        "mod_title": "Gameplay Overhaul",
        "is_pk4": false,
        "sources": ["shared", "bfg"],
        "base_path": "D:\\RBDOOM-3-BFG",
        "game": "gameplayoverhaul",
        "zip_name": "rbdoom3_gameplayoverhaul",
        "pk4_name": null,
        "should_deploy": true
    },
    {
        "game_title": "Classic RBDOOM 3 BFG",
        "mod_title": "Gameplay Overhaul",
        "is_pk4": false,
        "sources": ["shared", "bfg"],
        "base_path": "D:\\Classic-RBDOOM-3-BFG",
        "game": "gameplayoverhaul",
        "zip_name": "rbdoom3_gameplayoverhaul",
        "pk4_name": null,
        "should_deploy": false
    },
    {
        "game_title": "dhewm 3",
        "mod_title": "Gameplay Overhaul",
        "is_pk4": true,
        "sources": ["shared", "d3"],
        "base_path": "D:\\dhewm3",
        "game": "d3xp",
        "zip_name": "doom3_gameplayoverhaul",
        "pk4_name": "zzzgameplayoverhaul",
        "should_deploy": false
    },
    {
        "game_title": "fhDOOM",
        "mod_title": "Gameplay Overhaul",
        "is_pk4": true,
        "sources": ["shared", "d3"],
        "base_path": "D:\\fhDOOM",
        "game": "gameplayoverhaul",
        "zip_name": "doom3_gameplayoverhaul",
        "pk4_name": "zzzgameplayoverhaul",
        "should_deploy": false
    },
    {
        "game_title": "Doom 3",
        "mod_title": "Gameplay Overhaul",
        "is_pk4": true,
        "sources": ["shared", "d3"],
        "base_path": "D:\\SteamLibrary\\steamapps\\common\\Doom 3",
        "game": "gameplayoverhaul",
        "zip_name": "doom3_gameplayoverhaul",
        "pk4_name": "zzzgameplayoverhaul",
        "should_deploy": true
    }
]
```

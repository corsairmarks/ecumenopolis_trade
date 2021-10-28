# Overview

Tired of your city-planets not being top-tier trading hubs? Then this mod is for you! This mod adds an "Ecumenopolis Commercial" colony designation that boosts the build-speed of commercial buildings and commercial arcologies by 25% and overall trade value by 20%.  That is the same trade value boost as Urban Worlds, Trade Stations, and Commercial Ring Worlds.

Because Stellaris version 3.1 added the +20% trade value boost to the base Ecumenopolis colony designation, we went back to the drawing board to double down on the theme of a commercial megacity.  Now choosing to use the Ecumenopolis Commercial colony designation additionally enables construction of the new "Commercial Arcology" district which provides Merchant and Clerk jobs.  If you change the colony designation later, you'll keep any existing Commercial Arcologies but lose some of the Merchant jobs and be unable to build more Commercial Arcologies until the designation is switched back to Ecumenopolis Commercial.

Commercial Arcologies provide more Merchant jobs and fewer Clerk jobs as long as the colony designation remains Ecumenopolis Commercial.  But wait, there's more!  Empires with the Merchant Guilds civic will find that more Merchants replace Clerks.  But wait, there's _even_ more!  Megacorps replace some Clerks with Executives and Managers.  And if that wasn't enough, we'll throw in positive interaction with the "Commercial Enterprise" tradition for even more Merchants, Executives, and Managers.

# Changes

Adds the `col_ecu_trade` colony type and a new district `district_arcology_commercial`.

## Localisation

* English by corsairmarks (author)
* Russian (Русский) by [NCTribit](https://steamcommunity.com/id/0418282)

## Compatibility

Practically any mod, as long as it doesn't entirely remove ecumenopoleis or create the same colony type.

Built for Stellaris version 3.1.* "Lem."  Not compatible with achievements.

### When to Install

This mod can be safely added to your savegame after the game has started.  Because it adds a new district for planets, it is not advisable to remove during gameplay.  Back up your savegame before trying to remove a mod.

## Changelog

* 1.0.0 Initial version
* 2.0.0 Updated for Stellaris 3.1.* "Lem" - icons are assign differently (and better)
* 2.1.0 Add "Commercial Arcology" district and a colony automation plan
* 2.2.0 Enhancements based on user feedback
    * Allow Commercial Arcologies on empire any capital that is also an ecumenopolis
    * Move bonus trade value generated in concert with starbase modules, etc from each district to the colony designation - it was a bit too strong for each district to generate loads of trade value regardless of employment
* 2.3.0 Add Russian localisation
* 2.3.1 Tweak colony automation

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/ecumenopolis_trade)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.
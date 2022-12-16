# Overview

Tired of your city-planets not being top-tier trading hubs? Then this mod is for you! This mod adds an "Ecumenopolis Commercial" colony designation that boosts the build-speed of commercial buildings and commercial arcologies by 25% and overall trade value by 20%.  That is the same trade value boost as Urban Worlds, Trade Stations, and Commercial Ring Worlds.

Because Stellaris version 3.1 added a +20% trade value boost to the base Ecumenopolis colony designation, I went back to the drawing board to double down on the theme of a commercial megacity.  That lead to the creation of the new "Commercial Arcology" district which provides Merchant and Clerk jobs.  Choosing to use the Ecumenopolis Commercial colony designation also swaps some Clerk jobs into Merchant jobs from each Commercial Arcology, and can provide small amounts of bonus trade if you meet varying hidden, trade-related conditions - see if you can figure them out.

But wait, there's more!  Empires with the Merchant Guilds civic will find that more Merchants replace Clerks.  But wait, there's _even_ more!  MegaCorps replace a Clerk with a Manager and a Merchant with an Executive (all those Clerks need bossing around).  And if that wasn't enough, we'll throw in positive interaction with the "Commercial Enterprise" tradition for even more Merchants!

# Changes

Adds the `col_ecu_trade` colony type and a new district `district_arcology_commercial`.  Overrides the `col_ecu_mix` colony type to match the bonuses for the default mixed ringworld (+20% immigration pull, +5% jobs output, +5% Pop growth/assembly) so as to not conflict (mechanics-wise) with the new `col_ecu_trade` type.  Overwrites trade colony automation `automate_trade_planet` in order to include `col_ecu_trade` and exclude `col_ecu_mix`.

## Localisation

* English by corsairmarks (author)
* Polish (Polskie) by [Gatzek](https://steamcommunity.com/profiles/76561198440146604)
* Russian (Русский) by [NCTribit](https://steamcommunity.com/id/0418282)

## Compatibility

Practically any mod, as long as it doesn't entirely remove ecumenopoleis or create/edit the same colony types.  Compatible with Planetary Diversity.

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.

### Required Dependency Mods

In order to see and interact with the new commercial arcology district, it is necessary to use a UI mod that allows more districts to be visible.  [UI Overhaul Dynamic](https://steamcommunity.com/sharedfiles/filedetails/?id=1623423360) and [Bigger Planet View](https://steamcommunity.com/sharedfiles/filedetails/?id=1587178040) are two possible options.  If you play Stellaris on a lower resolution (such as 1366x768 or 1600x900) there are not many mod offerings that show many districts without making the planetview too large, so I created [Basic Planetview: More Districts](https://steamcommunity.com/sharedfiles/filedetails/?id=2654043078) to solve that issue.

### Recommended Companion Mods

[Enhanced Trade Districts and Designations](https://steamcommunity.com/sharedfiles/filedetails/?id=2641081470) to upgrade the trade-focused colony designations and districts for habitats and ringworlds.

### When to Install

This mod can be safely added to your savegame after the game has started.  Because it adds a new district for planets, it is not advisable to remove during gameplay.  Back up your savegame before trying to remove a mod.

### Known Issues

Overwriting a colony type produces an error log.  Expect to see two entries in error.log similar to these:

```
[23:10:05][game_singleobjectdatabase.h:165]: Object with key: col_ecu_mix already exists, using the one at  file: common/colony_types/01_ecumenopolis_trade_colony_types_overrides.txt line: 2
[23:10:09][game_singleobjectdatabase.h:165]: Object with key: has_trade_designation already exists, using the one at  file: common/scripted_triggers/10_ecumenopolis_trade_scripted_triggers_ai_overrides.txt line: 2
```

## Changelog

* 1.0.0 Initial version
* 2.0.0 Updated for Stellaris 3.1 "Lem" - icons are assign differently (and better)
* 2.1.0 Add "Commercial Arcology" district and a colony automation plan
* 2.2.0 Enhancements based on user feedback
    * Allow Commercial Arcologies on empire any capital that is also an ecumenopolis
    * Move bonus trade value generated in concert with starbase modules, etc from each district to the colony designation - it was a bit too strong for each district to generate loads of trade value regardless of employment
* 2.3.0 Add Russian localisation
* 2.4.0 Further ecumenopolis refinements
    * Tweak colony automation
    * Alter the basic "Ecumenopolis" colony designation to provide different bonuses
    * Commercial Arcologies also grant +3 Clerk jobs with the tradition "Interstellar Franchising"
* 2.4.1 Improved colony automation plan
* 2.4.2 Adjust colony designation weighting
* 2.5.0 Updated for Stellaris version 3.2 "Herbert" - no changes
* 2.6.0 Add Commercial Arcologies to Planetary Diversity's Palace and Corporate Ecumenopoleis
    * Special thanks to Gatzek for help with the correct special `district_set`s
    * Add Polish localisation by Gatzek
* 3.0.0 Update for Stellaris version 3.3 "Libra"
    * Use new triggers
    * Add README/description notes about now requiring a UI mod
    * Allow building Commercial Arcologies on any ecumenopolis
* 3.0.1 Add global flag to indicate that this mod is installed
* 4.0.0 Update for Stellaris version 3.4 "Cepheus"
    * Fix inaccurate description for the Ecumenopolis Commercial designation - it improves Commercial Arcologies, rather than enabling their construction (mechanics change in mod version 3.0.0)
    * Better code for the Ecumenopolis Commercial designation
    * Use memory optimization feature for a trigger
    * Replace old automation with an enhanced version of the new trade colony plan
    * Add automation plans for the `col_ecu_mix` colony type, because this mod removes the trade bonuses and removes it from the trade automation plan
* 4.1.0 Balance update - reduce the overwhelming **Trade Power™** generated for minimal effort and also simplify triggered job swaps
    * Reduce the amount of free MegaCorp job swaps; post-unity-rework they are much more powerful than in the past
    * Simplify Merchant jobs swaps - things got a little out of hand
    * Add custom description to the commercial district, describing the job shifts
* 5.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Bonus Clerk jobs are now tied to the tradition Trickle Up Economics instead of Interstellar Franchising (from underlying game changes)
    * Add override of new built-in trigger `has_trade_designation`, consume it for trade colony automation
    * Trade planet automation cooperates with my other trade-related district mods

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/ecumenopolis_trade)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.
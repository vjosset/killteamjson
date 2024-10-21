# killteamjson
JSON Dataset for Killteam 2021 Compendium, including additional teams from White Dwarf and boxed sets.

See also [KTDash](https://ktdash.app/) and its [API](https://github.com/vjosset/ktdash/blob/v2/docs/api.md)

"compendium.json" will hold the latest version of the full compendium.json

This repo may contain snapshots of the compendium to be used as backups.

**If you are using this dataset for your own applications, please give the appropriate credit. These teams take hours to load.**

# Structure/Hierarchy

The root of the JSON file is an array of "faction" objects.

- [Root] - Array of Faction objects
  - `factionid` - *string* - ID for this faction
  - `factionname` - *string* - Name of this faction
  - `description` - *string* - HTML description of this faction (flavor text)
  - `killteams` - Array of Killteam objects
    - `factionid` - *string* - ID for this killteam's faction
    - `killteamid` - *string* - ID for this killteam
    - `killteamname` - *string* - Name of this killteam
    - `description` - *string* - HTML description of this killteam (flavor text)
    - `killteamcomp` - *string* - HTML description of this killteam's composition
    - `equipments` - Array of Equipment objects
      - `factionid` - *string* - ID for this equipment's faction
      - `killteamid` - *string* - ID for this equipment's killteam
      - `eqid` - *string* - ID for this equipment
      - `eqpts` - *string* - Cost in Points of this equipment
      - `eqname` - *string* - Name of this equipment
      - `eqdescription` - *string* - HTML description of this equipment
    - `ploys`
      - `strat` - Array of strategic ploy objects
        - `factionid` - *string* - ID for this ploy's faction
        - `killteamid` - *string* - ID for this ploy's killteam
        - `ploytype` - *string* - Type of ploy (`S`: Strategic, `T`: Tactical)
        - `ployid` - *string* - ID of this ploy
        - `ployname` - *string* - Name of this ploy
        - `CP` - *string* - Cost in Command Points to run this ploy
        - `description` - *string* - HTML description of this ploy
      - `tac` - Array of tactical ploy objects
        - `factionid` - *string* - ID for this ploy's faction
        - `killteamid` - *string* - ID for this ploy's killteam
        - `ploytype` - *string* - Type of ploy (`S`: Strategic, `T`: Tactical)
        - `ployid` - *string* - ID of this ploy
        - `ployname` - *string* - Name of this ploy
        - `CP` - *string* - Cost in Command Points to run this ploy
        - `description` - *string* - HTML description of this ploy
    - `fireteams` - Array of fireteam objects
      - `factionid` - *string* - ID for this fireteam's faction
      - `killteamid` - *string* - ID for this fireteam's killteam
      - `fireteamid` - *string* - ID for this fireteam
      - `description` - *string* - HTML description of this fireteam (flavor text)
      - `fireteamname` - *string* - Name of this fireteam
      - `archetype` - *string* - Archetypes for this fireteam (separated by forward slash "/")
      - `fireteamcomp` - *string* - HTML description of this fireteam's composition
      - `operatives` - Array of Operative objects
        - `factionid` - *string* - ID for this operative's faction
        - `killteamid` - *string* - ID for this operative's killteam
        - `fireteamid` - *string* - ID for this operative's fireteam
        - `opid` - *string* - ID for this operative
        - `opname` - *string* - Name of this operative
        - `description` - *string* - HTML description of this operative (flavor text)
        - `M` - *string* - Movement characteristic. Holds placeholders for distance measurements (see below)
        - `APL` - *string* - Action Point Limit characteristic
        - `GA` - *string* - Group Activation characteristic
        - `DF` - *string* - Defense characteristic (number of Defense dice to roll when shot)
        - `SV` - *string* - Save characteristic
        - `W` - *string* - Wounds characteristic
        - `weapons` - Array of Weapon objects
          - `factionid` - *string* - ID for this weapon's faction
          - `killteamid` - *string* - ID for this weapon's killteam
          - `fireteamid` - *string* - ID for this weapon's fireteam
          - `opid` - *string* - ID for this weapon's operative
          - `wepid` - *string* - ID for this weapon
          - `wepname` - *string* - Name of this weapon
          - `weptype` - *string* - Weapon type (`R`: Ranged, `M`: Melee/Close Combat)
          - `Weaponprofiles` - Array of WeaponProfile objects
            - `factionid` - *string* - ID for this weapon profile's faction
            - `killteamid` - *string* - ID for this weapon profile's killteam
            - `fireteamid` - *string* - ID for this weapon profile's fireteam
            - `opid` - *string* - ID for this weapon profile's operative
            - `wepid` - *string* - ID for this weapon profile's weapon
            - `profileid` - *string* - ID for this weapon profile
            - `name` - *string* - Name of this weapon profile (usually blank if the weapon only has one profile)
            - `A` - *string* - Attacks characteristic
            - `BS` - *string* - Ballistic/Weapon Skill characteristic
            - `D` - *string* - Damage characteristic
            - `SR` - *string* - Comma-separated list of Special and Critical rules for this weapon profile

# Distance/Range Placeholders

- `[TRI]` - Triange range (1 inch) - Recommend replacing with `&#x25B2;` (&#x25B2;) in HTML output
- `[CIRCLE]` - Circle range (2 inches) - Recommend replacing with `&#x2B24;` (&#x2B24;) in HTML output
- `[SQUARE]` - Square range (3 inches) - Recommend replacing with `&#9632;` (&#9632;) in HTML output
- `[PENT]` - Pentagon range (6 inches) - Recommend replacing with `&#x2B1F;` (&#x2B1F;) in HTML output



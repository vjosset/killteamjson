# killteamjson
JSON Dataset for Killteam 2024.

See also [KTDash](https://ktdash.app/)

**If you are using this dataset for your own applications, please give the appropriate credit. These teams take hours to load.**

# Structure/Hierarchy

The root of the JSON file is an array of "killteam" objects.

- `killteams` - Array of Killteam objects
  - `factionId` - *string* - ID for this killteam's faction
  - `killteamId` - *string* - ID for this killteam
  - `killteamname` - *string* - Name of this killteam
  - `description` - *string* - Markdown description of this killteam (flavor text)
  - `composition` - *string* - Markdown description of this killteam's composition
  - `archetypes` - *string* - Slash-delimited list of archetypes for this killteam
  - `opTypes` - Array of OpType (operative type) objects
    - `killteamId` - *string* - ID for this operative type's killteam
    - `opTypeId` - *string* - ID for this operative type
    - `opTypeName` - *string* - Name of this operative type
    - `MOVE` - *string* - Movement characteristic.
    - `APL` - *string* - Action Point Limit characteristic
    - `SAVE` - *string* - Save characteristic
    - `WOUNDS` - *string* - Wounds characteristic
    - `keywords` - *string* - Comma-separated keywords for this operative type
    - `basesize` - *integer* - Base size for this operative type
    - `nameType` - *string* - Name generation key
    - `weapons` - Array of Weapon objects
      - `opTypeId` - *string* - ID for this weapon's operative
      - `wepId` - *string* - ID for this weapon
      - `wepName` - *string* - Name of this weapon
      - `wepType` - *string* - Weapon type (`R`: Ranged, `M`: Melee/Close Combat, `P`: Psychic, `E`: Equipment)
      - `profiles` - Array of WeaponProfile objects
        - `wepid` - *string* - ID for this weapon profile's weapon
        - `seq` - *integer* - Sequence/ordering number for this profile
        - `profileName` - *string* - Name of this weapon profile (usually blank if the weapon only has one profile)
        - `ATK` - *string* - Attacks characteristic
        - `HIT` - *string* - Hit characteristic
        - `DMG` - *string* - Damage characteristic ([Normal]/[Critical])
        - `WR` - *string* - Comma-separated list of Weapon Rules for this weapon profile
    - `abilities` - Array of Ability objects
      - `abilityId` - *string* - Unique ID for this ability
      - `opTypeId` - *string* - ID of the OpType that has this ability
      - `abilityName` - *string* - Name/title of this ability
      - `AP` - *integer* - The AP to spend to use this ability. If `null`, this is a passive ability.
      - `description` - *string* - Markdown-formatted description of this ability
    - `options` - Array of Option objects (e.g. Chapter Tactics for Angels of Death)
      - `optionId` - *string* - Unique ID for this option
      - `opTypeId` - *string* - ID of the OpType that has this option
      - `optionName` - *string* - Name/title of this ability
      - `description` - *string* - Markdown-formatted description of this option
      - `effects` - *string* - Coded string for effects to apply to the operative or its weapons
  - `ploys` - Array of Ploy objects
    - `ployId` - *string* - Unique ID for this ploy
    - `killteamId` - *string* - ID of the killteam this ploy belongs to
    - `seq` - *integer* - Sequence/ordering number for this ploy
    - `ployType` - *string* - The type of ploy: `S` for Strategy ploys, `T` or `F` for Firefight ploys (don't ask)
    - `ployName` - *string* - Name/title of this ploy
    - `description` - *string* - Markdown-formatted description of this ploy
  - `equipments` - Array of Equipment objects
    - `eqId` - *string* - Unique ID for this equipment
    - `killteamId` - *string* - ID of the killteam this equipment belongs to
    - `seq` - *integer* - Sequence/ordering number for this equipment
    - `eqName` - *string* - Name/title of this equipment
    - `description` - *string* - Markdown-formatted description of this ploy
    - `effects` - *string* - Coded string for effects to apply to operatives or weapons


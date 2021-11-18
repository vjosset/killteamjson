# killteamjson
JSON Dataset for Killteam 2021 Compendium

See also https://ktdash.app/factions.htm and https://ktdash.app/api/faction.php

The root of the JSON file is an array of "faction" objects.

Structure/Hierarchy:
- Faction
  - factionid
  - factionname
  - description
  - Killteams
    - factionid
    - killteamid
    - killteamname
    - description
    - killteamcomp
    - equipments
      - factionid
      - killteamid
      - eqid
      - eqpts
      - eqname
      - eqdescription
    - ploys
      - strategic ploys
        - factionid
        - killteamid
        - ploytype
        - ployid
        - ployname
        - CP
        - description
      - tactical ploys
        - factionid
        - killteamid
        - ploytype
        - ployid
        - ployname
        - CP
        - description
    - Fireteams
      - factionid
      - killteamid
      - fireteamid
      - description
      - fireteamname
      - archetype
      - fireteamcomp
      - Operatives
        - factionid
        - killteamid
        - fireteamid
        - opid
        - opname
        - description
        - M
        - APL
        - GA
        - DF
        - SV
        - W
        - Weapons
          - factionid
          - killteamid
          - fireteamid
          - opid
          - wepid
          - wepname
          - weptype
          - WeaponProfiles
            - factionid
            - killteamid
            - fireteamid
            - opid
            - wepid
            - profileid
            - name
            - A
            - BS
            - D
            - SR

"compendium.json" will hold the latest version of the full compendium.json

This repo may contain snapshots of the compendium to be used as backups

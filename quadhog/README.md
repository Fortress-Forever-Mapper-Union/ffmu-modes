# QUAD HOG

# by -\_YoYo178\_-

## STTS: Finished

### List of maps:
ff_qh_hold - a modified version of ff_hold (created by Alw1n)

(Available on `MaxTF - Classic server (EU, Nurnberg)`)

### Description:
Quad hog, An experiment run by unknown people, who are testing a 
very strong and highly unstable flag's behavior on players, which 
turns them into a blood-thirsty beast called the Quad Hog.

The Quad Hog vaporises if it does not get blood within 60 seconds.

### Objectives:
- For the Quad Hunters, kill the Quad Hog.
- For the Quad Hog, kill the Quad Hunters.

As simple as that.

### Tips:
- Quad Hog gains Quad Damage and his health and armor will regenerate while holding the flag.
- Quad Hog's health regeneration is percentual and varies between 5% and 10% depending on the number of players on the server.
- The Quad Hog can stay alive until 60 seconds without any kill.

### Setup:
Just add the line 
```lua
IncludeScript("base_quadhog")
```
into your map.lua file and that's it.



- **Note**: `base_quadhog` already includes functionalities of these:
```lua
IncludeScript("base_teamplay")
IncludeScript("base_location")
```

### Parameters/Tweaks

- **Note**: Values in parenthesis are default values.

- **Flag settings**:
    - `FLAG_THROW_SPEED` -- Initial speed of the flag when thrown. (`512`)
        - Type: `integer`
    - `FLAG_RETURN_TIME` -- Number of seconds after the flag should return to the middle. (`60`)
        - Type: `integer`

- **Scoring settings**:
    - `PERIOD_TIME` -- Add scores to the quad hog and his team every `x` seconds. (`10`)
        - Type: `integer`
    - `POINTS_PER_PERIOD` -- Amount of score to add to the quad hog's team per `PERIOD_TIME` seconds. (`1`)
        - Type: `integer`
    - `HOLDER_POINTS` -- Amount of Fortress Points to add to the quad hog per `PERIOD_TIME` seconds. (`100`)
        - Type: `integer`
    - `TEAM_MEMBER_POINTS` -- Amount of Fortress Points to add to each of the quad hog's team members per `PERIOD_TIME` seconds. (`50`)
        - Type: `integer`

- **Quad hog settings**:
    - `REGEN_TIME` -- Regenerates the quad hog every `x` seconds. (`1`)
        - Amount is 5% - 10% of maximum health and armor depending on the number of players on the server.
        - Type: `integer`
    - `DAMAGE_BONUS` -- Multiplies the quad hog's damage by `DAMAGE_BONUS` when holding the flag. (`4`)
        - 1 = Normal damage, 4 = Quad damage
        - Type: `integer`

- **Health bar settings**:
    - `HEALTH_BAR_ENABLED` -- If set to true, displays a health bar of the Quad Hog to the Quad Hunters. (`true`)
        - Type: `boolean`

- **Miscellaneous** **<ins>(SHOULD NOT BE OVERRIDDEN)</ins>**:

    ### <ins>These variables are used by the script's internal code and should **NOT** be overridden.</ins>

    - `REGENERATING_ENABLED` -- Defines when the quad hog's regeneration is enabled. (`true`)
        - Type: `boolean`
    - `QUADHUNTERS_TEAM` -- Quad Hunters team. (`Team.kBlue`)
        - Type: `integer`
    - `QUADHOG_TEAM` -- Quad hog team. (`Team.kRed`)
        - Type: `integer`
    - `FIRST_PLAYER_JOIN` -- Used by `player_spawn` to determine when to start counting the timer to open the barriers. (`false`)
        - Type: `boolean`
    - `QH` -- Contains the Quad Hog's casted `Player` object, and `nil` when the Quad Hog is dead.
        - Type: `Player`

    - Health bar critical variables:
        - `HEALTH_BAR_X` -- X position of the health bar. (`0`)
            - Type: `integer`
        - `HEALTH_BAR_Y` -- Y position of the health bar. (`35`)
            - Type: `integer`
        - `HEALTH_BAR_WIDTH` -- Width of the health bar. (`250`)
            - Type: `integer`
        - `HEALTH_BAR_HEIGHT` -- Height of the health bar. (`37`)
            - Type: `integer`
        - `HEALTH_BAR_ALIGN` -- Alignment of the health bar. (`4`)
            - Type: `integer`

        - `HEALTHBAR_HEALTH_X` -- X position of the health bar's health value. (`0`)
            - Type: `integer`
        - `HEALTHBAR_HEALTH_Y` -- Y position of the health bar's health value. (`40`)
            - Type: `integer`
        - `HEALTHBAR_HEALTH_WIDTH` -- Width of the health bar's health value. (`238`)
            - Type: `integer`
        - `HEALTHBAR_HEALTH_HEIGHT` -- Height of the health bar's health value. (`5`)
            - Type: `integer`
        - `HEALTHBAR_HEALTH_ALIGN` -- Alignment of the health bar's health value. (`4`)
            - Type: `integer`

        - `HEALTHBAR_ARMOR_X` -- X position of the health bar's armor value. (`0`)
            - Type: `integer`
        - `HEALTHBAR_ARMOR_Y` -- Y position of the health bar's armor value. (`54`)
            - Type: `integer`
        - `HEALTHBAR_ARMOR_WIDTH` -- Width of the health bar's armor value. (`210`)
            - Type: `integer`
        - `HEALTHBAR_ARMOR_HEIGHT` -- Height of the health bar's armor value. (`12`)
            - Type: `integer`
        - `HEALTHBAR_ARMOR_ALIGN` -- Alignment of the health bar's armor value. (`4`)
            - Type: `integer`


#### infoscripts
* `flag` -- The flag that grants the holder quad damage.

* `holdbasekit` contains:
    - 100 health
    
    -- respawn time 5s.

* `holdarmorkit` contains:
    - 200 armor

    -- respawn time 10s.

* `holdbasepack` contains:
    - 200 grenades ammo
    - 200 bullets
    - 200 nails
    - 200 shells
    - 200 rockets
    - 200 cells
    
    -- respawn time 5s.

* `holdhealthkit` contains:
    - 50 health

    -- respawn time 20s.

* `holdammopack` contains:
    - 50 armor
    - 20 grenades ammo
    - 100 bullets
    - 100 nails
    - 100 shells
    - 20 rockets
    - 100 cells

    -- respawn time 20s.

* `holdgrenpack` contains:
    - 10 grenades ammo
    - 50 bullets
    - 50 shells
    - 50 nails,
    - 5 rockets
    - 50 cells
    - 1 primary grenade
    - 1 secondary grenade.

	-- respawn time 30s.

#### triggerscripts
(none)
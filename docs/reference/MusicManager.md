# MusicManager

## Public Methods

| Method      | Description                          | Return type |
| ----------- | ------------------------------------ | ----------- |
| `#!cs ArenaMusicEnd()` | WIP | `#!cs void` |
| `#!cs ArenaMusicStart` | WIP | `#!cs void` |
| `#!cs FilterMusic()` | WIP | `#!cs void` |
| `#!cs ForceStartMusic()` | WIP | `#!cs void` |
| `#!cs ForceStopMusic()` | WIP | `#!cs void` |
| `#!cs PlayBattleMusic()` | WIP | `#!cs void` |
| `#!cs PlayBossMusic()` | WIP | `#!cs void` |
| `#!cs PlayCleanMusic()` | WIP | `#!cs void` |
| `#!cs StartMusic()` | WIP | `#!cs void` |
| `#!cs StopMusic()` | WIP | `#!cs void` |
| `#!cs UnfilterMusic()` | WIP | `#!cs void` |

## Private Methods

| Method      | Description                          | Return type |
| ----------- | ------------------------------------ | ----------- |
| `#!cs OnEnable()` | Is called when the object gets enabled | `#!cs void` |
| `#!cs RemoveHighPass()` | WIP | `#!cs void` |
| `#!cs Update()` | Is called each frame | `#!cs void` |

## Public fields

| Field       | Type    | Description                          |
| ----------- | ------- | ------------------------------------ |
| `#!cs battleTheme` | `#!cs AudioClip` | The music that gets overlayed when enemies are present in a level |
| `#!cs bossTheme` | `#!cs AudioClip` | The music that gets used when there is a boss. Only used in some levels |
| `#!cs cleanTheme` | `#!cs AudioClip` | The default music that is used when there are no enemies |
| `#!cs dontMatch` | `#!cs bool` | WIP |
| `#!cs fadeSpeed` | `#!cs float` | WIP |
| `#!cs forcedOff` | `#!cs bool` | WIP |
| `#!cs off` | `#!cs bool` | WIP |
| `#!cs requestedThemes` | `#!cs float` | WIP |
| `#!cs targetTheme` | `#!cs AudioSource` | WIP |
| `#!cs volume` | `#!cs float` | WIP |

## Private fields

| Field       | Type    | Description                          |
| ----------- | ------- | ------------------------------------ |
| `#!cs allThemes` | `#!cs AudioSource[]` | WIP |
| `#!cs arenaMode` | `#!cs bool` | WIP |
| `#!cs defaultVolume` | `#!cs float` | WIP |
| `#!cs filtering` | `#!cs bool` | WIP |
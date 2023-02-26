---
title: CheckHurtException
---

# [EnemyIdentifier](../).CheckHurtException

Function in `EnemyIdentifier` / Returns `bool`

### Description
Checks if an attacker enemy can't hurt a receiver enemy. For example, Strays can't hurt Stalkers, but Swordmachines can. **Returns false if it can't hurt it, so SM and Stalker would return false**.

### Decleration
`public static bool CheckHurtException(`[`EnemyType`](../../EnemyType)` attacker, `[`EnemyType`](../../EnemyType)` receiver)`

### Parameters
|Name|Description|
|-|-|
|`attacker`|The enemy attacking the receiver|
|`receiver`|The enemy which is getting attacked.|

### Usage 
```cs
void SandifyEnemy(EnemyIdentifier eid) 
{
    // If an enemy can attack a stalker, it gets sandified.

    if (!EnemyIdentifier.CheckHurtException(eid.enemyType, EnemyType.Stalker)) 
    {
        eid.Sandify();
    }
}
```
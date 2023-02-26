---
title: Unbless
---

# [EnemyIdentifier](../).Unbless

Function in `EnemyIdentifier` / Returns `void`

### Description
Unbless an enemy, optionally only visually.

### Decleration
`public void Unbless(bool visualOnly = false)`

### Parameters
|Name|Description|
|-|-|
|`visualOnly`|If this is true, the enemy will only unbless visually.|

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, unbless the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Unbless();
    }
}
```
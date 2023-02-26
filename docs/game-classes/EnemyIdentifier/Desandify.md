---
title: Desandify
---

# [EnemyIdentifier](../).Desandify

Function in `EnemyIdentifier` / Returns `void`

### Description
Desandifies an enemy, optionally only visually.

### Decleration
`public void Desandify(bool visualOnly = false)`

### Parameters
|Name|Description|
|-|-|
|`visualOnly`|If this is true, the enemy will only desandify visually.|

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, desandify the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Desandify();
    }
}
```
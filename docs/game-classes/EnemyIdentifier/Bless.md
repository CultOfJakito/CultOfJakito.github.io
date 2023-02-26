---
title: Bless
---

# [EnemyIdentifier](../).Bless

Function in `EnemyIdentifier` / Returns `void`

### Description
Blesses the enemy, what did you think?

### Decleration
`public void Bless(bool ignorePrevious = false)`

### Parameters
|Name|Description|
|-|-|
|`ignorePrevious`|If this is false, it won't bless the enemy if it is aleady blessed. If true, it will do it again.|

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, bless the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Bless();
    }
}
```
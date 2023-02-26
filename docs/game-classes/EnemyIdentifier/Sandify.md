---
title: Sandify
---

# [EnemyIdentifier](../).Sandify

Function in `EnemyIdentifier` / Returns `void`

### Description
Makes the enemy sandified.

### Decleration
`public void Sandify(bool ignorePrevious = false)`

### Parameters
|Name|Description|
|-|-|
|`ignorePrevious`|If this is false, it won't sandify the enemy if it is aleady sandified. If true, it will do it again.|

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, sandify the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Sandify();
    }
}
```
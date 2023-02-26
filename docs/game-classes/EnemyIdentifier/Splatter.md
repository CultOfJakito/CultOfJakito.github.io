---
title: Splatter
---

# [EnemyIdentifier](../).Splatter

Function in `EnemyIdentifier` / Returns `void`

### Description
Kills the enemy as if it had died from fall damage.

### Decleration
`public void Splatter()`

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, kill the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Splatter();
    }
}
```
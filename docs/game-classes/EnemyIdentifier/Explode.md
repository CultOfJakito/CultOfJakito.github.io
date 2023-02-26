---
title: Explode
---

# [EnemyIdentifier](../).Explode

Function in `EnemyIdentifier` / Returns `void`

### Description
Explodes and kills the enemy.

### Decleration
`public void Explode()`

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, explode the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Explode();
    }
}
```
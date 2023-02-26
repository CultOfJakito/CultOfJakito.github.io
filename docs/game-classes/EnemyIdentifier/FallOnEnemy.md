---
title: FallOnEnemy
---

# [EnemyIdentifier](../).FallOnEnemy

Function in `EnemyIdentifier` / Returns `void`

### Description
Makes the enemy act as if Maurice was falling on it. Some will [`Explode`](../Explode), others will dodge.

### Decleration
`public static void FallOnEnemy(EnemyIdentifier eid)`

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, bless the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        EnemyIdentifier.FallOnEnemy(eidid.eid);
    }
}
```
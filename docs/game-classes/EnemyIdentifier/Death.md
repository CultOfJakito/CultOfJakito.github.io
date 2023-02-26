---
title: Death
---

# [EnemyIdentifier](../).Death

Function in `EnemyIdentifier` / Returns `void`

### Description
Kills the enemy but without any enemy-specific death behaviour. This means Drones suiciding, Maurices falling, Idols and Virtues exploding, etc.

### Decleration
`public void Death()`

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If an enemy limb is touched, kill the enemy it belongs to.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.Death();
    }
}
```
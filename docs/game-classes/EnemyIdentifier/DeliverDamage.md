---
title: DeliverDamage
---

# [EnemyIdentifier](../).DeliverDamage

Function in `EnemyIdentifier` / Returns `void`

### Description
Hurts an enemy, or heals it if the value is negative. This function is pretty intimidating, because the amount of arguments, but it's not that bad.

### Decleration
`public void DeliverDamage(GameObject target, Vector3 force, Vector3 hitPoint, float multiplier, bool tryForExplode, float critMultiplier = 0f, GameObject sourceWeapon = null)` (this is insanely long)

### Parameters
|Name|Description|
|-|-|
|`target`|The specific body part the enemy got hit at. If you just want to hurt the enemy, pass in the `EnemyIdentifier.gameObject`, as all it needs is a `EnemyIdentifierIdentifier` on a child. |
|`force`|The direction the enemy got hit in, determines where a Drone goes when crashing or how hard and where a Filth gets knocked back. You can just do `Vector3.zero`.|
|`hitPoint`|Where the enemy got hit, and where gore will spawn from. You can just do `EnemyIdentifier.transform.position`.|
|`multiplier`|How much damage will be done. This isn't exact, as it will be multiplied depending on other factors (e.g. if it's a limb hit).|
|`tryForExplode`|If this is true and the enemy's health reaches zero, `EnemyIdentifier.Explode()` will be called, instead of `EnemyIdentifier.Death()`.|
|`critMultiplier`|How much critical hits are multiplied by. If you hit an enemy in the arm, it will do `multiplier + (0.5 * multiplier * critMultiplier)` (0.5 being the hardcoded damage multiplier for limb hits; for headshots, it is 1). Default value is 0.|
|`sourceWeapon`|What weapon was used, used for style meter degradation. Default is null.|

### Usage 
```cs
void OnCollisionEnter(Collision col) 
{
    // If you touch an enemy, hurt it for one damage.

    EnemyIdentifierIdentifier eidid;

    if (col.gameObject.TryGetComponent(out eidid)) 
    {
        eidid.eid.DeliverDamage(eidid.gameObject, Vector3.zero, eidid.transform.position, 1, false);
    }
}
```
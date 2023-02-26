# EnemyIdentifier

Class in `Assembly-CSharp` / Inherits from [`MonoBehaviour`](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html) / Implemented in `Assembly-CSharp`

### Description
This class is a `MonoBehaviour` component, and is on every enemy in the game.
It lets you do many things, such as hurting and healing enemies, sandifying them, and blessing them.

### Public Functions
|Method|Description|
|-|-|
|[`Bless`](Bless)|Will bless the enemy.|
|[`Death`](Death)|Will instantly kill an enemy, without doing any enemy specific actions. Also see [`InstaKill`](InstaKill).|
|[`DeliverDamage`](DeliverDamage)|Lets you damage enemies, and heal them if the value is negative.|
|[`Desandify`](Desandify)|Will desandify an enemy, or disable just the sand visuals.|
|[`DestroyMagnets`](DestroyMagnets)|Destroys all magnets on the enemy.|
|[`Explode`](Explode)|The enemy will die and explode.|
|`ForceGetHealth`|Updates the health value. This is called in `Update`, so it's completely useless.|
|[`InstaKill`](InstaKill)|Will kill an enemy and do enemy specific actions, like Maurices falling, or drones suiciding. Also see [`Death`](Death)|
|[`Sandify`](Sandify)|Will sandify an enemy.|
|[`Splatter`](Splatter)|Kills the enemy, while also making an explosion of blood, like it fell at a high speed.|
|`StopSplatter`|Removes rigidbody constraints for the enemy's limbs. Useless.|
|[`Unbless`](Unbless)|Will unbless an enemy, or disable just the bless visuals.|

### Static Functions
|Method|Description|
|-|-|
|[`CheckHurtException`](CheckHurtException)|Will check if an [`EnemyType`](../EnemyType) is allowed to hurt another [`EnemyType`](../EnemyType).|
|[`FallOnEnemy`](FallOnEnemy)|Called when a Maurice touches an enemy while falling. Will either explode the enemy, or make it dodge (e.g. Mindflayers).|
# EnemyType

Enum in `Assembly-CSharp` / Implemented in `Assembly-CSharp`

### Description
This is an enum with every enemy in the game. Don't ask me what the numbers are for, because I don't know.

### Usage
```cs
void HurtEnemy(EnemyIdentifier eid) 
{
    // If the enemy is a Cancerous Rodent, bless it. Otherwise, sandify it.
    
    if (eid.enemyType == EnemyType.CancerousRodent) 
    {
        eid.Bless();
    } 
    else 
    {
        eid.Sandify();
    }
}
```

### Properties
|Property|Value|
|-|-|
|CancerousRodent|23|
|Cerberus|0|
|Drone|
|Ferryman|26|
|Filth|3|
|FleshPrison|17|
|Gabriel|16|
|GabrielSecond|28|
|HideousMass|2|
|Idol|21|
|Leviathan|27|
|MaliciousFace|4|
|Mandalore|25|
|Mindflayer|5|
|Minos|11|
|MinosPrime|18|
|Schism|14|
|Sisyphus|19|
|Soldier|15|
|Stalker|12|
|Stray|
|Streetcleaner|6|
|Swordsmachine|
|Turret|20|
|V2|8|
|V2Second|22|
|VeryCancerousRodent|24|
|Virtue|9|
|Wicked|
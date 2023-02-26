---
title: DestroyMagnets
---

# [EnemyIdentifier](../).DestroyMagnets

Function in `EnemyIdentifier` / Returns `void`

### Description
Destroys all the magnets on an enemy.

### Decleration
`public void DestroyMagnets()`

### Usage 
```cs
void Update() 
{
    // Make it so that magnets are destroyed every frame.

    GetComponent<EnemyIdentifier>().DestroyMagnets();
}
```
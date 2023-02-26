<a name='assembly'></a>
# Assembly-CSharp

## Contents

- [NewMovement](#T-NewMovement 'NewMovement')
  - [activated](#F-NewMovement-activated 'NewMovement.activated')
  - [ActivatePlayer()](#M-NewMovement-ActivatePlayer-- 'NewMovement.ActivatePlayer()')
  - [DeactivatePlayer()](#M-NewMovement-DeactivatePlayer-- 'NewMovement.DeactivatePlayer()')

<a name='T-NewMovement'></a>
## NewMovement `type`

##### Namespace



##### Summary

The main player class. Responsible for movement, health/damage mechanics, player VFX, etc.

<a name='F-NewMovement-activated'></a>
### activated `constants`

##### Summary

Whether or not the player is currently active. It is not recommended to write to this value directly; instead use [ActivatePlayer](#M-NewMovement-ActivatePlayer-- 'NewMovement.ActivatePlayer()') and [DeactivatePlayer](#M-NewMovement-DeactivatePlayer-- 'NewMovement.DeactivatePlayer()')

<a name='M-NewMovement-ActivatePlayer--'></a>
### ActivatePlayer() `method`

##### Summary

Activates the player, the [CameraController](#T-CameraController 'CameraController') instance, and the [GunControl](#T-GunControl 'GunControl') and [FistControl](#T-FistControl 'FistControl') instances.

##### Parameters

This method has no parameters.

<a name='M-NewMovement-DeactivatePlayer--'></a>
### DeactivatePlayer() `method`

##### Summary

Deactivates the player, the [CameraController](#T-CameraController 'CameraController') instance, and the [GunControl](#T-GunControl 'GunControl') and [FistControl](#T-FistControl 'FistControl') instances.

##### Parameters

This method has no parameters.

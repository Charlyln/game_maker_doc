#  Projectile
Create a object `obj_bullet`.
-  **Create Event**
```js
audio_play_sound(snd_bullet, 1, false)
direction = point_direction(x, y, mouse_x, mouse_y);
speed = 15;
image_angle = direction;
```
-  **Collision**
```js
with (obj_enemy) {
	hp -= 1;
}
instance_destroy();

```
> This object target mouse position and when it collide with an enemy, it will remove him 1 hp, then bullet destroy. The sound `snd_bullet` play on bullet creation.
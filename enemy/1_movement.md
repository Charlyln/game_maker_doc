
#  Movement
Create a object `obj_enemy`.
-  **Create Event**
```js
move_speed = 2;
hp = 3;
```
-  **Step Event**
```js
if (instance_exists(obj_player)) {
	move_towards_point(obj_player.x, obj_player.y, move_speed);
}
if (hp < 1) {
	audio_play_sound(snd_death, 1, false);
    instance_create_layer(x, y, "lyr_loot", obj_loot);
    instance_destroy();
}
```
> This enemy will move towards player position. When he's dead, it will play a sound, it will drop an item `obj_loot` and destroy his instance.

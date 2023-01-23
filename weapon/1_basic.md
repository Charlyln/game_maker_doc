#  Weapon
Create a object `obj_weapon`.
-  **Create Event**
```js
cooldown_rate = 15
cooldown = cooldown_rate
```
-  **Step Event**
```js
shoot = mouse_check_button(mb_left);

if (shoot && cooldown < 1 && bullet_in_magazine > 0) {
	instance_create_layer(x, y, "lyr_bullet", obj_bullet);
	cooldown = cooldown_rate;
}
cooldown -= 1;
```
> This object will create 1 projectile every 15 frames but without reload logic. You need to create `lyr_bullet` layer and `obj_bullet` object.
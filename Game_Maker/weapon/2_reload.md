#  Weapon
Create a object `obj_weapon`.
-  **Create Event**
```js
cooldown_rate = 15;
cooldown = cooldown_rate;
magazine_capacity = 6;
bullet_in_magazine = magazine_capacity;
reload_time = 60;
reloading = false;

```
-  **Step Event**
```js
shoot = mouse_check_button(mb_left);

if (shoot && cooldown < 1 && bullet_in_magazine > 0) {
	instance_create_layer(x, y, "lyr_bullet", obj_bullet);
	cooldown = cooldown_rate;
	bullet_in_magazine -= 1;
}
cooldown -= 1;

if (bullet_in_magazine < 1 && !reloading) {
	reloading = true;
	alarm[0] = reload_time;
}

```
-  **Alarm 0**
```js
bullet_in_magazine = magazine_capacity;
reloading = false;

```
> After the object fire 6 bullets, it will take 60 frames to reload.   
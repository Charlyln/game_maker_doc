
#  Movement

-  **Create Event**
```js
move_speed = 2
```
-  **Script or Create Event**
```js
press = function (key) {
	return keyboard_check(ord(key))
}
```

-  **Step Event**
```js
move_up =  press("Z") || press("W")
move_left = press("A") || press("Q")
move_down = press("S")
move_right = press("D")

if (move_up) y -= moove_speed
if (move_down) y += moove_speed
if (move_left) x -= moove_speed
if (move_right) x += moove_speed
```
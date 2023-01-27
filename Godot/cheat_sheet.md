# SCRIPTS

-   ##### `$`:

    -   is shorthand for `get_node()`. So in the code above, `$AnimatedSprite.play()` is the same as `get_node("AnimatedSprite").play()`.

-   ##### `clamp()`:

    -   function that prevent object moving to leave the screen. `clamp(value: float, min: float, max: float)`.

-   ##### `delta`:
    -   The `delta` parameter in the `_process()` function refers to the frame length - the amount of time that the previous frame took to complete. Using this value ensures that your movement will remain consistent even if the frame rate changes.

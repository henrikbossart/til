If your div has a dynamic/undefined width and/or height, then instead of the `margin`, set the `transform` to the negative half of the div's relative width and height.

```css
position: fixed;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
```
 # Transforms Property
 *Transforms property provided by CSS to control and position elements. The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values*


 # Transform Syntax
 *The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses. Look at the following example that rotate the element 45 degree using transform property.*

```
 div {
  transform: rotate(45deg);
  
}

```


## 2D Transforms:
*Changing element on two dimensions ( x and y): here are somethings that you can change using 2D Transforms:*

- *2D Rotate: The rotate value provides the ability to rotate an element from 0 to 360 degrees(like in the previous example)*


- *2D Scale: Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger. look at the following example*
```

.box-1 {
  transform: scale(.75);
}
```
*this example changed the size of an element to 75 percent of it's original size.*

### Note that you can add x or y values to the scale property to change the size either in vertically or horizantally .

&nbsp;


- *2D Translate: to shift the element in any direction . look at the example that try to shift the element 10 degree to the left*

```

.box-1 {
  transform: translateX(-10px);
}

```
&nbsp;

# 3D Transforms
*changing the element in three dimensional scale (x , y and z) .  here are somethings that you can change using 3D Transforms:*

- *3D Rotate: With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.*

*Using the rotateX value allows you to rotate an element around the x axis, as if it were being bent in half horizontally. Using the rotateY value allows you to rotate an element around the y axis, as if it were being bent in half vertically. Lastly, using the rotateZ value allows an element to be rotated around the z axis.*


- *3D Translate: Elements may also be translated on the z axis using the translateZ value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element.*


- *3D Scale:By using the scaleZ three-dimensional transform elements may be scaled on the z axis. This isn’t extremely exciting when no other three-dimensional transforms are in place, as there is nothing in particular to scale. In the demonstration below the elements are being scaled up and down on the z axis, however the rotateX value is added in order to see the behavior of the scaleZ value. When removing the rotateX in this case, the elements will appear to be unchanged*




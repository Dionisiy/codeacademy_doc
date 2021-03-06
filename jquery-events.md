### **Review of jQuery Events**

The setup almost always looks like this:

`$(document).ready(function() {
    $('thingToTouch').event(function() {
        $('thingToAffect').effect();
    });
});`

where "thing to touch" is the HTML element you'll click on, hover over, or otherwise interact with, and "thing to affect" is the HTML element that fades away, changes size, or undergoes some other transformation.

Sometimes these elements are one and the same—you might hover over a`<div>` to change its opacity. Other times, you might interact with a separate element; for example, you might click on a button to resize a`<div>`.

Sometimes if you want an effect to occur right away, without an event like`.click()` or `.hover()`, you'll skip the second line in the above:

```
$(document).ready(function() {
    $('thingToAffect').effect();
});
```

### **Combining .click\(\) and .hover\(\)**

Well done! Let's add one more jQuery event to our "destruction of Krypton" simulation. Krypton didn't just vanish, it exploded! Let's make it turn red.

```
$('div').hover(function(){
  $('div').addClass('green');
});
```

### **The .dblclick\(\) Event**

Now that we've reviewed our jQuery event handlers, let's learn a new one.

### **Hover**

What if you wanted to create an effect when your mouse is on top of an object, then have that effect vanish when your mouse moved away? You might notice this effect in use on many site's navigation bars!

```
$('div').hover(
    function(){
      $(this).addClass('highlight');
   },
   function(){
      $(this).removeClass('highlight');
   }
);
```

1. We first select the element we want to modify `$('div')`
2. Secondly notice that our `hover`effect is able to take two `functions(){}`separated by a comma. The comma is very important!
3. The first `function(){}` we pass will be run when we first mouse over our target. Here we apply a class of`highlight`
4. The second `function(){}` will be called when our mouse leaves the object. This is where we remove the class `highlight`

Your second `function(){}` doesn't have to be the opposite of the first`function(){}`, but it would be very common!

### **Let's .focus\(\)!**

Another event we can make use of is`.focus()`. We say an element has **focus**when we click on it or tab over to it. If you've ever filled out a form on a web page and seen how each text box lights up when you tab to it or click on it, you've seen focus in action!

The `.focus()` event handler only works on elements that can receive focus—the list of these elements is a bit vague, but HTML elements like`<textarea>`s and `<input>`s are the usual suspects.

### **The .keydown\(\) Event**

The `.keydown()` event is triggered whenever a key on the keyboard is pressed. It only works on whatever page element has focus, so you'll need to click on the window containing your div before pressing a key in order for you to see its effects.

Let's go ahead and combine our new event with a new effect: `.animate()`! We'll use this to move an object on the screen whenever we press a key.

The `.animate()` effect takes two inputs: the animation to perform, and the time in which to perform the animation. Here's an example:

```
$(document).ready(function() {
   $('div').animate({left:'+=10px'},500);
});
```

This will take the first div it finds and move it ten pixels to the right. Remember, increasing the distance from the left margin moves something to the right; the `+=` bit is just a shorthand for "take the existing number and add ten to it." In this case, it add ten pixels to the current distance from the left margin.

### **Filling Out the Cases**

Every key press on a keyboard is translated into a number for the computer to use. Don't worry about memorizing them, for now we've given you the basics in `script.js`

```
/ Left arrow key pressed
case 37:
  ('img').animate({left: "-=10px"}, 'fast');
```

1. The left arrow key on our keyboards translates to number 37 to the computer. When that key is pressed, we animate our image to the left by subtracting `10px`
2. To move up we subtract `10px` from the `top`
3. To move right we add `10px` to the`left`
4. Finally, to move down we add `10px`to the `top`






# **Selecting Elements**

The most basic concept of jQuery is to "select some elements and do something with them." jQuery supports most CSS3 selectors, as well as some non-standard selectors. For a complete selector reference, visit the [Selectors documentation on api.jquery.com](http://api.jquery.com/category/selectors/).

### **Selecting Elements by ID**

```
$( "#myId" ); // Note IDs must be unique per page.
```

### **Selecting Elements by Class Name**

```
$( ".myClass" );
```

### **Selecting Elements by Attribute**

```
$( "input[name='first_name']" );
```

### **Selecting Elements by Compound CSS Selector**

```
$( "#contents ul.people li" );
```

### **Selecting Elements with a Comma-separated List of Selectors**

```
$( "div.myClass, ul.people" );
```

### **Pseudo-Selectors**

```
$( "a.external:first" );
$( "tr:odd" );

// Select all input-like elements in a form (more on this below).
$( "#myForm :input" );
$( "div:visible" );

// All except the first three divs.
$( "div:gt(2)" );

// All currently animated divs.
$( "div:animated" );
```

> **Note:** When using the `:visible` and `:hidden` pseudo-selectors, jQuery tests the actual visibility of the element, not its CSS `visibility` or `display` properties. jQuery looks to see if the element's physical height and width on the page are both greater than zero.
> 
> However, this test doesn't work with `<tr>` elements. In the case of `<tr>` jQuery does check the CSS `display` property, and considers an element hidden if its `display` property is set to `none`.

### **Choosing Selectors**

Choosing good selectors is one way to improve JavaScript's performance. Too much specificity can be a bad thing. A selector such as `#myTable thead tr th.special` is overkill if a selector such as `#myTable th.special` will get the job done.

### **Does My Selection Contain Any Elements?**

Once you've made a selection, you'll often want to know whether you have anything to work with. A common mistake is to use:

```
// Doesn't work!
if ( $( "div.foo" ) ) {
    ...
}
```





# css display properties 

As we know that display properties is essential part of css layout where we want to render our elements
layout in different ways 

# lets talk a little bit of css display properties which are listed below
* display :block 
* display :inline-block 
* display :inline 
* display :contents 
* display :flex
* display :grid 
* display :table 
* display :none 
* display :initial
* display :inherit

*There are lots of others display properties but above are enought to use in your real world projects*

display of block -It seperate the elements to new line and takes full width and height its height and width can be changed.

inline-It doesnot goes to newline so it stick on the same line .It width and height cannot be changed. 

inline-block -Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values

grid -display elements as  block level elements.

inline-flex	Displays an element as an inline-level flex container.

inline-grid	Displays an element as an inline-level grid container

list-item	Let the element behave like a ```<li>``` 

none	The element is completely 

initial	Sets this property to its default

inherit	Inherits this property from its parent element.


# This was the quick recap of css display properties the main thing and most used display propeties are block inline flexbox and grid focus on this .

# ```index.html```
```html

<div class="flexbox">
        <ul>
            <li>Cook food</li>
            <li>goes for shopping</li>
            <li>order food online</li>
            <li>Learn new skills</li>
        </ul>
    </div>
```
```css
/* flexbox unidirection one dimension 1D*/

.flexbox{
    display: flex;
    justify-content: center;
    align-items: center;
}
.flexbox ul{
    display: flex;
}
.flexbox ul li{
    margin:0 10px;
    font-size:clamp(1.2rem,1.4rem,1.5rem);
    list-style:none;
}


```

*lets see grid a 2D layout columns rows*

# ```index.html```
```html

<h1 class="grid-heading">Grid display properties</h1>
<div class="grid">
    <div class="box box1"></div>
    <div class="box box2"></div>
    <div class="box box3"></div>
    <div class="box box4"></div>
    <div class="box box5"></div>
</div>

```

# ```style.css```

```css
/* grid */

.grid-heading{
    text-align: center;
    font-style:italic;
    margin:10px 0;
}
.grid{
    display: grid;
    background:lightblue;
    max-width:300px;
    min-height:300px;
    margin:20px auto;
}

.box{
    margin:10px;
}
.box:nth-child(1){
    background:rgba(27, 5, 148, 0.603);
}
.box:nth-child(2){
    background:rgba(2, 138, 63, 0.664);
}
.box:nth-child(3){
    background:lightyellow;
}
.box:nth-child(4){
    background:crimson;
}
.box:nth-child(5){
    background:rgba(27, 20, 20, 0.486);
}


```

# ```index.html```
```html

<div class="container">
        <div class="children">
            <h1>Talk to senior developer</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil, incidunt?</p>
        </div>
    </div>
```

# ```style.css```
```css
/* container */



.children{
    /* display:; */
    /* inline doesnot work in block you have to do inline-block so that it behaves like inline and could not take full height and width  */
    background:linear-gradient(45deg ,red,blue,green);
    border-radius:4px;
    margin:20px 3rem;

    
}


```
# initial(means by default black) and inherit(respect to parent)

# ```index.html```
```html

   <!-- initial display example -->
    <div class="initial">
        <h1>Initial display properties</h1>
        <p>The initial div container is given the color of blueviloet and its changed to all the sibling inside div changes to blueviolet but as soon as the any elements inside our div is changed to color of properties to initial it will go to its initial color which is black by default.</p>
    </div>

    <!-- inherit -->
    <div class="inherit">
        <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis, quo?</h1>
    </div>
    <div class="inherit1">
        <h3>You can see this color gets changed because we set the inherit1 div of color lightcoral and we inherit the child h3 to take the parent color</h1>
    </div><div class="inherit2">
        <h3>Here we apply the same logic as we did above on second div</h1>
    </div>

```
```css

/* inherit */

h3{
    color:lightseagreen;

}
.inherit1{
   color:lightcoral;
}

.inherit1 h3{
    color:inherit;
    /* h3 will inherit it color from its parents which inherit1 of color lightcoral */
}

/* inherit2 */
.inherit2 {
    color:cornflowerblue;
    border:1px solid rgb(0 0 0 /.3);
    
}
.inherit2 h3{
    color:inherit;
}


```

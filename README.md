# CSS Diner

**Note:** Everything in this document is based off of the [CSS Diner](http://flukeout.github.io/) game intended to help developers become more familiar with CSS selectors. This "companion" is simply meant to be used as a supplement/reference.

**Goal of game:** Select the "wiggling items" using CSS selectors.

**Selectors:** Go to the [CSS selector descriptions and examples](#css-selector-descriptions-and-examples) section to refresh your memory on a variety of CSS selectors.

**Usage:** For any given level, you are provided with a `.gif` illustrating what you are trying to select. Here is how you should go about using this companion if you do not simply go [the site](http://flukeout.github.io/) hosting the game:
1. **Watch:** Watch the `.gif` to see what is wiggling.
2. **HTML Viewer:** Open (i.e., click) the `HTML Viewer` to see what HTML actually makes up the `.gif` you saw in Step 1. This will be important because you will be trying to target or select *named* elements, and you may need to see the HTML to deduce these elements' names, what classes or attributes they may have, etc.
3. **Hint:** Click the `Hint` if you need a nudge in the right direction. What you find in the hint will often be phraseology that more or less points you to a specific part of the [CSS selector descriptions and examples](#css-selector-descriptions-and-examples) section.
4. **CSS Viewer:** Click the `CSS Viewer` to see one (or more) potential solutions. You may come up with completely different solutions! If so, consider making a pull request to this repo with your additional solution formatted as seen in the provided solution(s). 

## Levels

- [Level 1](#level-1)    
- [Level 2](#level-2)    
- [Level 3](#level-3)    
- [Level 4](#level-4)    
- [Level 5](#level-5)    
- [Level 6](#level-6)    
- [Level 7](#level-7)    
- [Level 8](#level-8)    
- [Level 9](#level-9)    
- [Level 10](#level-10)    
- [Level 11](#level-11)    
- [Level 12](#level-12)    
- [Level 13](#level-13)    
- [Level 14](#level-14)    
- [Level 15](#level-15)    
- [Level 16](#level-16)    
- [Level 17](#level-17)    
- [Level 18](#level-18)    
- [Level 19](#level-19)    
- [Level 20](#level-20)    
- [Level 21](#level-21)    
- [Level 22](#level-22)    
- [Level 23](#level-23)    
- [Level 24](#level-24)    
- [Level 25](#level-25)    
- [Level 26](#level-26)    
- [Level 27](#level-27)    
- [Level 28](#level-28)    
- [Level 29](#level-29)    
- [Level 30](#level-30)    
- [Level 31](#level-31)    
- [Level 32](#level-32)

## CSS Selector Descriptions and Examples

- [Type](#type)        
- [ID Selector](#id-selector)        
- [Descendant Selector](#descendant-selector)        
- [Combine Descendant and ID Selectors](#combine-descendant-and-id-selectors)        
- [Class Selector](#class-selector)        
- [Combining the Class Selector with Other Selectors](#combining-the-class-selector-with-other-selectors)
- [Combining Selectors with Commas](#combining-selectors-with-commas)        
- [Universal Selector](#universal-selector)        
- [Adjacent Sibling Selector](#adjacent-sibling-selector)        
- [General Sibling Selector](#general-sibling-selector)        
- [Child Selector](#child-selector)        
- [First Child Pseudo-selector](#first-child-pseudo-selector)        
- [Only Child Pseudo-selector](#only-child-pseudo-selector)        
- [Last Child Pseudo-selector](#last-child-pseudo-selector)        
- [Nth Child Pseudo-selector](#nth-child-pseudo-selector)        
- [Nth Last Child Selector](#nth-last-child-selector)        
- [First of Type Selector](#first-of-type-selector)        
- [Nth of Type](#nth-of-type)        
- [Nth of Type Selector with Formula](#nth-of-type-selector-with-formula)        
- [Only of Type](#only-of-type)        
- [Last of Type](#last-of-type)        
- [Empty](#empty)        
- [Negation Pseudo-class](#negation-pseudo-class)        
- [Attribute Selector (general)](#attribute-selector-general)       
- [Attribute Selector (specific)](#attribute-selector-specific)        
- [Attribute Value Selector](#attribute-value-selector)        
- [Attribute Starts With Selector](#attribute-starts-with-selector)        
- [Attribute Ends with Selector](#attribute-ends-with-selector)        
- [Attribute Wildcard Selector](#attribute-wildcard-selector)

### Type

```css
A
```

Selects all elements of type `A`. Type refers to the type of tag, so `<div>`, `<p>`, and `<ul>` are all different element types. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

div {
    /* style all <div> elements */
}

p {
    /* style all <p> elements */
}
```

</details>

### ID Selector

```css
#id
```

Selects an element with a specific `id`. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

#cool {
    /* style the element with id="cool" */
}

/* you can also combine the ID selector with the type selector */

ul#long {
    /* style the element <ul id="long"> */
}
```

</details>

### Descendant Selector

```css
A B
```

Selects all elements `B` that are children of `A`; that is, `A B` is how you select an element(s) `B` that is inside another element `A`.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

p strong {
    /* style <strong> elements that are children of <p> elements */
}

#fancy span {
    /* style any <span> elements that are inside of the element with id="fancy" */
}
```

</details>

### Combine Descendant and ID Selectors

```css
#id A
```

You can combine any selector with the descendant selector.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

#cool span {
    /* style all <span> elements that are inside of the element with id="cool" */
}
```

</details>

### Class Selector

```css
.classname
```

Select elements by their class. The class selector selects all elements with that class attribute. Elements can only have one ID, but many classes.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

.neato {
    /* style all elements with class="neato" */
}
```

</details>

### Combining the Class Selector with Other Selectors

```css
A.className
```

You can combine the class selector with other selectors, like the type selector.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

ul.important {
    /* style <ul> elements that have class="important" */
}

#big.wide {
    /* style the element with id="big" that also has class="wide" */
}
```

</details>

### Combining Selectors with Commas

```css
A, B
```

You can select all `A` and `B` elements (or all `A`, `B`, and `C` elements with `A, B, C`, etc.). 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

p, .fun {
    /* style all <p> elements as well as all elements with class="fun" */
}

a, p, div {
    /* style all <a>, <p>, and <div> elements */
}
```

</details>

### Universal Selector 

```css
*
```

You can select all elements with the universal selector `*` (also known as a wildcard).

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

p * {
    /* style all elements inside of all <p> elements */
}

ul.fancy * {
    /* style every element inside all <ul class="fancy"> elements */
}
```

</details>

### Adjacent Sibling Selector

```css
A + B
```

This selects all `B` elements that direct follow `A` elements. Elements that follow one another are called siblings. They're on the same level or depth. In the HTML markup, elements that are siblings should have the same indentation level.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

p + .intro {
    /* styles every element with class="intro" that directly follows a <p> */
}

div + a {
    /* style every <a> element that directly follows a <div> */
}
```

</details>

### General Sibling Selector

```css
A ~ B
```

Selects all elements `B` that follow an element `A`; that is, you can select all siblings of an element that follow it. This is sort of like the adjacent sibling selector (i.e., `A + B`) except `A ~ B` gets *all* of the following sibling elements instead of just the direct next one. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

div.main-intro ~ p {
    /* style all elements <p> after <div class="main-intro"> that are on the same level as the div */
}
```

</details>

### Child Selector

```css
A > B
```

Selects all `B` that are direct children of `A`. You can select elements that are direct children of other elements. A child element is any element that is nested directly in another element. Elements that are nested deeper than that are called descendant elements.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

div#container > ul {
    /* style all <ul> elements that are children of <div id="container"> */
}
```

</details>

### First Child Pseudo-selector

```css
A:first-child
```

Selects all first-child elements that are of type `A`. A child element is any element that is directly nested in another element. You can combine this pseudo-selector with other selectors.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

:first-child {
    /* style all first child elements */
}

p:first-child {
    /* style all first child <p> elements  */
}

div p:first-child {
    /* style all first child <p> elements that are in a <div> */
}
```

</details>

### Only Child Pseudo-selector

```css
A:only-child
```

Selects any element `A` that is the only element inside of another one. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

span:only-child {
    /* style the <span> elements that are the only child of some other element */
}

div p:only-child {
    /* style the <p> inside any <div> so long as the <p> is the only one of its kind */
}
```

</details>

### Last Child Pseudo-selector

```css
A:last-child
```

Selects any element `A` that is the last child of another element. You can use this selector to select an element that is the last child element inside of another element.

<details><summary> Example(s)</summary>

```css
:last-child {
    /* style all last-child elements */
}

span:last-child {
    /* style all last-child <span> elements */
}

ul li:last-child {
    /* style the last <li> element inside every <ul> */
}
```

</details>

### Nth Child Pseudo-selector

```css
:nth-child(A)
```


Selects the nth (i.e., 1st, 3rd, 12th, etc.) child element in another element.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

:nth-child(8) {
    /* style every element that is the 8th child of another element */
}

div p:nth-child(2) {
    /* style the second <p> in every <div> */
}
```

</details>

### Nth Last Child Selector

```css
:nth-last-child(A)
```

Selects the children from the bottom of the parent. This is like nth-child but counting from the back. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

:nth-last-child(2) {
    /* styles all second-to-last child elements */
}
```

</details>

### First of Type Selector

```css
A:first-of-type
```

Selects the first element of type `A` within another element.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES*/

span:first-of-type {
    /* style the first <span> in any element */
}
```

</details>

### Nth of Type 

```css
A:nth-of-type(num)
```

Selects an element of type `A` based on its order in another element (or `even` or `odd` instances of that element).

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

div:nth-of-type(2) {
    /* style the second instance of a <div> */
}

.example:nth-of-type(odd) {
    /* style all odd instances of elements with class="example" */
}
```

</details>

### Nth of Type Selector with Formula

```css
:nth-of-type(An+B)
```

The nth-of-type formula selects every nth element, starting the count at a specific instance of that element.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

span:nth-of-type(6n+2) {
    /* style every 6th instance of a <span>, starting from (and including) the second instance */
}
```

</details>

### Only of Type

```css
:only-of-type
```

Selects the only element of its type within another element.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

p span:only-of-type {
    /* selects a <span> within any <p> if it is the only <span> in there */
}
```

</details>

### Last of Type 

```css
:last-of-type
```

Selects each last element of that type within another element. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

div:last-of-type {
    /* styles the last <div> in every element */
}

p span:last-of-type {
    /* styles the last <span> in every <p> */
}
```

</details>

### Empty

```css
:empty
```

Selects elements that don't have any other elements inside of them.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

div:empty {
    /* style all empty <div> elements */
}
```

</details>

### Negation Pseudo-class

```css
:not(X)
```

Selects all elements that do not match the negation selector. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

:not(#fancy) {
    /* style all elements that do not have id="fancy" */
}

div:not(:first-child) {
    /* style every <div> that is not a first child */
}

:not(.big, .medium) {
    /* style all elements that do not have class="big" or class="medium" */
}
```

</details>

### Attribute Selector (general)

```css
[attribute]
```

Selects all elements that have a specific attribute. Attributes appear inside the opening tag of an element. For example: `<span attribute="value"></span>`. An attribute does not always have a value, it can be blank.

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

a[href] {
    /* style all <a> elements that have an href attribute */
}

[type] {
    /* style all elements that have a type attribute */
}
```

</details>

### Attribute Selector (specific)

```css
A[attribute]
```

Selects all elements `A` that have a specific attribute. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

[value] {
    /* style all elements that have a value attribute */
}

a[href] {
    /* style all <a> elements that have an href attribute */
}

input[disabled] {
    /* styles all <input> elements with the disabled attribute */
}
```

</details>

### Attribute Value Selector

```css
[attribute="value"]
```

Selects all elements that have a specific attribute value. Attribute selectors are case sensitive. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

input[type="checkbox"] {
    /* style all <input> elements with type="checkbox" */
}
```

</details>

### Attribute Starts With Selector

```css
[attribute^="value"]
```

Selects all elements with an attribute value that starts with specific characters.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

.toy[category^="Swim"] {
    /* style elements with class toy and with attribute category="Swim[...]" */
}
```

</details>

### Attribute Ends with Selector

```css
[attribute$="value"]
```

Selects all elements with an attribute value that ends with specific characters.

<details><summary> Example(s)</summary>

```css
/* EXAMPLE */

img[src$=".jpg"] {
    /* style all images with a .jpg extension */
}
```

</details>

### Attribute Wildcard Selector

```css
[attribute*="value"]
```

Selects all elements with an attribute value that contains specific characters. 

<details><summary> Example(s)</summary>

```css
/* EXAMPLES */

img[src*="/thumbnails/"] {
    /* style all image elements that show images from the "thumbnails" folder */
}

[class="heading"] {
    /* style all elements with "heading" in their class, like class="main-heading" and class="sub-heading" */
}
```

</details>

## Level 1

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate />
    <plate />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302956-abecda80-db4a-11e9-8815-e61b632392d5.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

In the HTML, we see that each plate is represented by `<plate />`. How can we select an element by type?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate
```

</details>

## Level 2

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento />
    <plate />
    <bento />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302958-ac857100-db4a-11e9-90a7-dfc3b823d67b.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Note how each bento box is represented by `<bento />` in the HTML. Is there a way to select elements by type?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento
```

</details>

## Level 3

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate id="fancy" />
    <plate />
    <bento />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302959-ac857100-db4a-11e9-8d01-14f9c11b64fc.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Only one element in an HTML document should have a given `id`. How can you select an element by its `id`?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
/* solution 1 */
#fancy /* select any element with id="fancy" */

/* solution 2 */
plate#fancy /* select the plate element with id="fancy" */
```

</details>

## Level 4

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento />
    <plate>
        <apple />
    </plate>
    <apple />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302960-ac857100-db4a-11e9-960d-7995fe142af4.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

The apple is on the plate, and this implies that the apple is a descendent of the plate. How can you select a descendant `B` of an element `A`?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate apple
```

</details>

## Level 5

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento>
        <orange />
    </bento>
    <plate id="fancy">
        <pickle />
    </plate>
    <plate>
        <pickle />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302961-ac857100-db4a-11e9-8fdc-1b653ae25339.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

The HTML shows that the pickle is a descendant of the plate with `id=fancy`. 

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
#fancy pickle
```

</details>

## Level 6

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <apple />
    <apple class="small" />
    <plate>
        <apple class="small" />
    </plate>
    <plate />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302962-ac857100-db4a-11e9-953b-44826d443057.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Do the small apples share a common class name?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
apple.small
```

</details>

## Level 7

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <apple />
    <apple class="small" />
    <bento>
        <orange class="small" />
    </bento>
    <plate>
        <orange />
    </plate>
    <plate>
        <orange class="small" />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302963-ac857100-db4a-11e9-97ba-6ceda2f60df9.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

We do not want to select all objects with a class of `small`. Can we select only the oranges that have a class of `small` though?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
orange.small
```

</details>

## Level 8

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento>
        <orange />
    </bento>
    <orange class="small" />
    <bento>
        <orange class="small" />
    </bento>
    <bento>
        <apple class="small" />
    </bento>
    <bento>
        <orange class="small" />
    </bento>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302964-ac857100-db4a-11e9-9fa3-1232efddf2fe.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

We want the small oranges on bentos. How can we target what is on a bento? How can we target properties of what are on bentos? 

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento orange.small
```

</details>

## Level 9

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <pickle class="small" />
    <pickle />
    <plate>
        <pickle />
    </plate>
    <bento>
        <pickle />
    </bento>
    <plate>
        <pickle />
    </plate>
    <pickle />
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302965-ad1e0780-db4a-11e9-9aa8-38a3724d3be2.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we select multiple elements at once?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate, bento
```

</details>

## Level 10

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <apple />
    <plate>
        <orange class="small" />
    </plate>
    <bento />
    <bento>
        <orange />
    </bento>
    <plate id="fancy" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302966-ad1e0780-db4a-11e9-8373-d5eb101a8edc.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible for us to select everything at once?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
*
```

</details>

## Level 11

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate id="fancy">
        <orange class="small" />
    </plate>
    <plate>
        <pickle />
    </plate>
    <apple class="small" />
    <plate>
        <apple />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302967-ad1e0780-db4a-11e9-83e5-ce0940bda8e5.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we select all of the children of an element?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate *
```

</details>

## Level 12

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento>
        <apple class="small" />
    </bento>
    <plate />
    <apple class="small" />
    <plate />
    <apple />
    <apple class="small" />
    <apple class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302968-ad1e0780-db4a-11e9-8c2a-0a5dbf51a474.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we select each `apple` that is directly adjacent to a `plate`?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate + apple
```

</details>

## Level 13

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <pickle />
    <bento>
        <orange class="small" />
    </bento>
    <pickle class="small" />
    <pickle />
    <plate>
        <pickle />
    </plate>
    <plate>
        <pickle class="small" />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302969-ad1e0780-db4a-11e9-880f-918d4e2cfe8d.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

We want to select *all* of the `pickle` siblings after the `bento`.

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento ~ pickle
```

</details>

## Level 14

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate>
        <bento>
            <apple />
        </bento>
    </plate>
    <plate>
        <apple />
    </plate>
    <plate />
    <apple />
    <apple class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302971-ad1e0780-db4a-11e9-914f-28d20891e941.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

We do not want to select just any apple that is on a plate--we want to select the apple that is *directly* on the plate.

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate > apple
```

</details>

## Level 15

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento />
    <plate />
    <plate>
        <orange />
        <orange />
        <orange />
    </plate>
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302972-ad1e0780-db4a-11e9-89bb-a53dbbd75882.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

We know we want to select the `orange` that is the *first child* of the *plate*. A pseudo-selector may be appropriate here ....

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate orange:first-child
```

</details>

## Level 16

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate>
        <apple />
    </plate>
    <plate>
        <pickle />
    </plate>
    <bento>
        <pickle />
    </bento>
    <plate>
        <orange class="small" />
        <orange />
    </plate>
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302973-ad1e0780-db4a-11e9-9045-edfb9133d544.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we select multiple things at once? How can we select the *only* child of an element?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate apple:only-child, plate pickle:only-child
```

</details>

## Level 17

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate id="fancy">
        <apple class="small" />
    </plate>
    <plate />
    <plate>
        <orange class="small" />
        <orange />
    </plate>
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302974-ad1e0780-db4a-11e9-8a71-3c06231fe26c.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

There are multiple ways to do this. One somewhat contrived way is to think that the `apple` is the *last child* of the fancy `plate` and that the `pickle` is also, in some sense, the *last child* of its kind.

Alternatively, we really just want the child of the fancy `plate` that is an `apple` that is `small` as well as the `pickle` that is `small`.

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
/* Solution 1 */
plate#fancy apple:last-child, pickle:last-child /* contrived */

/* Solution 2 */
#fancy apple.small, pickle.small /* realistic */
```

</details>

## Level 18

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate />
    <plate />
    <plate />
    <plate id="fancy" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302975-ad1e0780-db4a-11e9-80a1-daae72343838.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible for us to select a specific child of a certain element?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate:nth-child(3)
```

</details>

## Level 19

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate />
    <bento />
    <plate>
        <orange />
        <orange />
        <orange />
    </plate>
    <bento />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302976-ad1e0780-db4a-11e9-9e5b-3a55fa26305c.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

It may be obvious to use `bento:first-of-type` here, but can we conjure up a more contrived solution such as counting from the back? For example, counting from the last `bento`, we see that the `bento` we want to select is really the third child. How can we select this `bento` in terms of "last children"?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento:nth-last-child(3)
```

</details>

## Level 20

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <orange class="small" />
    <apple />
    <apple class="small" />
    <apple />
    <apple class="small" />
    <plate>
        <orange class="small" />
        <orange />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302977-ad1e0780-db4a-11e9-95a8-1347351caa6f.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible for us to select the first element that is of a certain type?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
apple:first-of-type
```

</details>

## Level 21

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate />
    <plate />
    <plate />
    <plate />
    <plate id="fancy" />
    <plate />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302978-adb69e00-db4a-11e9-903e-b246acdc8ad0.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we use the pseduo-selector `nth-of-type` to our advantage here? What kinds of parameters does this pseudo-selector accept?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate:nth-of-type(even)
```

</details>

## Level 22

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate />
    <plate>
        <pickle class="small" />
    </plate>
    <plate>
        <apple class="small" />
    </plate>
    <plate />
    <plate>
        <apple />
    </plate>
    <plate />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302980-adb69e00-db4a-11e9-890a-2ab390ee5b5e.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Can we specify a selection pattern for certain types? That is, can we do something of the following sort: "Select every 4th instance of `plate`, starting at instance 2?" 

Way we would write the above is `plate:nth-of-type(4n+2)`

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate:nth-of-type(2n+3)
```

</details>

## Level 23

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate id="fancy">
        <apple class="small" />
        <apple />
    </plate>
    <plate>
        <apple class="small" />
    </plate>
    <plate>
        <pickle />
    </plate>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302981-adb69e00-db4a-11e9-9a3f-f8065b53cd36.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select a plate that only has a *single* child of the `apple` type?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate > apple:only-of-type
```

</details>

## Level 24

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <orange class="small" />
    <orange class="small" />
    <pickle />
    <pickle />
    <apple class="small" />
    <apple class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302982-adb69e00-db4a-11e9-9173-1b4fc6faf2c2.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

How can we select multiple elements that are the last of their type?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
orange:last-of-type, apple:last-of-type
```

</details>

## Level 25

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento />
    <bento>
        <pickle class="small" />
    </bento>
    <plate />
    <bento />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302983-adb69e00-db4a-11e9-9bfe-a813f1b03e3d.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible for us to select all types of an element that do not have children (i.e., are empty)?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento:empty
```

</details>

## Level 26

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate id="fancy">
        <apple class="small" />
    </plate>
    <plate>
        <apple />
    </plate>
    <apple />
    <plate>
        <orange class="small" />
    </plate>
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302984-adb69e00-db4a-11e9-80b9-9ad131e1287d.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select an element type that does *not* have a certain class?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
apple:not(.small)
```

</details>

## Level 27

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento>
        <apple class="small" />
    </bento>
    <apple for="Ethan" />
    <plate for="Alice">
        <pickle />
    </plate>
    <bento for="Clara">
        <orange />
    </bento>
    <pickle />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302985-adb69e00-db4a-11e9-86a1-3a27c2360d94.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select general elements based on whether or not those elements have certain attributes?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
[for]
```

</details>

## Level 28

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate for="Sarah">
        <pickle />
    </plate>
    <plate for="Luke">
        <apple />
    </plate>
    <plate />
    <bento for="Steve">
        <orange />
    </bento>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302986-adb69e00-db4a-11e9-9256-92f436d26810.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select only specific elements that have certain attributes?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
plate[for]
```

</details>

## Level 29

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <apple for="Alexei" />
    <bento for="Albina">
        <apple />
    </bento>
    <bento for="Vitaly">
        <orange />
    </bento>
    <pickle />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302987-adb69e00-db4a-11e9-96f8-af84b6c5919b.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select an element not only based on it having a certain attribute but also the value of that attribute?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento[for="Vitaly"]
```

</details>

## Level 30

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <plate for="Sam">
        <pickle />
    </plate>
    <bento for="Sarah">
        <apple class="small" />
    </bento>
    <bento for="Mary">
        <orange />
    </bento>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302988-adb69e00-db4a-11e9-83a8-d0ede4256872.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select elements that have an attribute whose value *starts* with a specified set of characters?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
*[for^="Sa"]
```

</details>

## Level 31

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <apple class="small" />
    <bento for="Hayato">
        <pickle />
    </bento>
    <apple for="Ryota" />
    <plate for="Minato">
        <orange />
    </plate>
    <pickle class="small" />
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302990-adb69e00-db4a-11e9-81ed-89b45fee3f17.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select elements that have an attribute whose value *ends* with a specified set of characters?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
*[for$="ato"]
```

</details>

## Level 32

<details><summary> HTML Viewer</summary>

```html
<div class="table">
    <bento for="Robbie">
        <apple />
    </bento>
    <bento for="Timmy">
        <pickle />
    </bento>
    <bento for="Bobby">
        <orange />
    </bento>
</div>
```

</details>

<img src="https://user-images.githubusercontent.com/52146855/65302991-ae4f3480-db4a-11e9-8497-8307e8aa11c7.gif"/>

<details><summary> Hint (or see <a href="#css-selector-descriptions-and-examples"> selector reference</a>)</summary>

Is it possible to select elements that have an attribute whose value *contains* a specified set of characters?

</details>

<details><summary> CSS Viewer (i.e., possible solution(s))</summary>

```css
bento[for*="obb"]
```

</details>
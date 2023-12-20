# IDMX-268 Final Project - Alex O'Neill


### 1. Using Ideas from Style Tile:

While I decided to ditch the color pallete I had previously decided on while creating my style tile, I chose to keep the font selection that I had decided on. Here are the fonts I used listed below in CSS.

```
body h1 {
    font-family: "Bebas Neue";
    font-size: 48pt;
}

body h2 {
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 16pt;
}

.skip-link {
    font-family: "Rockwell";
    font-size: 18pt;
}
```


### 2. Reset Used:

I used a reset/normalize library to create my project. Listed below is the reset I used in CSS.

```
@import "https://unpkg.com/open-props";
@import "https://unpkg.com/open-props/buttons.min.css";
@import "https://unpkg.com/open-props/masks.corner-cuts.min.css";

html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
}

/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
    display: block;
}

body {
    line-height: 1;
}

ol,
ul {
    list-style: none;
}

blockquote,
q {
    quotes: none;
}

blockquote:before,
blockquote:after,
q:before,
q:after {
    content: '';
    content: none;
}

table {
    border-collapse: collapse;
    border-spacing: 0;
}
```


### 3. Using Mobile Style Stage Code:

The base code that I built upon for this project is the same code that I used for my mobile style stage, albeit with a few adjestments made to the color pallete of the stage for both accessibility and aesthetic purposes. Below is the mobile style stage URL for you to visit and compare if you wish to do so.

[Click here for Mobile Style Stage Repo](https://github.com/RVCC-IDMX/ss-mobile-ao-g00298371)

 ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ ^ 



### 4. Fluid Spacing on Nav Bar:

For the spacing on the navigation bar, I found flex/justify to be an ineficient display method. Instead, what I did was that I displayed it as a grid and used grid-display-template and minmax (as suggested by Stephanie Eckles) to stretch it out. I then used grid-gap to space the elements out evenly. Listed below is the CSS.

```
.nav-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(10ch, 1fr));
    list-style: none;
    padding: 2;
    margin: 0;
    grid-gap: 1rem;
    background-color: hsl((var(--nav-color)));
    border-radius: 1rem;
}
```


### 5. Hover Effects on Nav Bar Links:

For the link styling on the navigation bar, I added hover and focus effects so that when you hovered over a link on the navigation bar, the color inverted and it, making the text color the background and the background color the text. The CSS for this is shown below.

```
.nav-list a {
    text-decoration: none;
    color: hsl ((var(--white)));
}

.nav-list a:hover,
.nav-list a:focus {
    color: hsl((var(--nav-color)));
    background-color: hsl((var(--bg-color)));
    border-radius: 0.5rem;
    outline: none;
    padding: 1em;
}
```


### 6. Custom Color Properties in HSL:

The way in which I used custom properties for my project was by creating a root folder with all the HSL values for the colors I was going to use in the project as labelled values. Shown below are the root folder and an application for the background color using the respective property in CSS.

```
:root {
    --black: 0, 0%, 0%;
    --white: 0, 0%, 100%;
    --bg-color: 53, 100%, 95%;
    --nav-color: 68, 10%, 40%;
    --link-color: 156, 92%, 24%;
}

html {
    background-color: hsl((var(--bg-color)));
}
```


### 7. Smooth Scroll Page Animation:

For the smooth scroll animation, I called back to my "About Me" project from my IDMX-225 course I took in the fall semester of last year. I created an HTML tag in CSS and simply dictated the scroll behaviour from there. CSS is listed below.

```
html {
    scroll-behavior: smooth;
}
```


### 8. Link Styling:

For the links, I removed the ugly default font and underline and replaced them with weighted Montserrat font styling and a subtle green color. CSS can be seen below.

```
a,
li a,
p a {
    text-decoration: none;
    color: hsl((var(--link-color)));
    font-weight: 600;
}

.nav-list a {
    text-decoration: none;
    color: hsl ((var(--white)));
}
```


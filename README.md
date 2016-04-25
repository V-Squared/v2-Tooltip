# v2-Tooltip
*SVG and HTML responsive Angular Tooltip Directive. Supports: Touch Screen, Mouse Over, Links and HTML in Tooltip.*

# Table of Contents
- [Key Features](#features)
- [v2-Tooltip Demo](#demo)
- [Distribution of v2-Tooltip](#disti)
- [How to make it work](#how-to)
- [User Story of Tooltips making long content fun](#user-story)
- [Reference](#reference)



# Key Features <a name="features"></a>
- **Lightweight:** Only 7 kB (not minimized) and minimum CPU load
- **Angular Directive:** Reusable and easy to use. 
- **SVG Support:** Easy to add Tooltips to SVG due to minimal code. See → [SVG Tooltip Code Example](#code-svg)
- **HTML Support:** Same Tooltip Plugin for SVG and HTML makes Tooltips consistent and easier to maintain.
- **Responsive:** All works as expected on any screen size. Supporting all features it was not as easy as it might appear.
- **Touchscreen Support:** All features work on touchscreen. Including link in Tooltip.
- **Intuitive to use:** All features are intuitively accessible. No explanation / help needed.
- **Link in Tooltip:** E.g. a "Read More" link for the reader who wants to know more than the Tooltip can offer. → [more](#link-in-tooltip)
- **Sanitized HTML in Tooltip:** Links, Pictures, Styling. All supported in v2-Tooltip.
- **Easy styling of Tooltip:** With its CSS.


# v2-Tooltip Demo <a name="demo"></a>
## Demo
- [Interactive Puzzle with Tooltips and Links](http://v-squared.github.io/#delivering-puzzle)
 
## Features of Demo
- **Open Tooltip**
   - **On PC:** Hover over puzzle to get Tooltip
   - **On Tablet:** Tab the Puzzle piece to get Tooltip
- **Using the Link:** 
   - **On PC:** Move mouse swiftly to hiver over tooltip. Then click link.
   - **On Tablet:** Tab the link in the Tooltip.
- **Responsive**
   - **Any Screeen Size:** Works on all screen sizes ranging from mobile phone to big screen
   - **Scaling support:** If SVG is bigger than screen size it scales down to fit. All Tooltip locations are scaled accordingly.
- **Show Selection:** When entering a shape it instantly shows that it is selected by changing the background color. (*1)

(*1) Technically this is not a feature of the v2-Tooltip, but it is a feature that any SVG tooltip implementation should have to help the user understand which element the tooltip refers to.



# Distribution of v2-Tooltip <a name="disti"></a>
## Angular Code
v2-Tooltip is an [Angular](https://angularjs.org/) Directive. 

## CSS Code
Contains all styling of the Tooltip.





# How to make it work <a name="how-to"></a>
At a later point we will create gh-pages site with short code examples and working demos and a tutorial. But until then please refer to the [working demo](http://v-squared.github.io/#delivering-puzzle). This is the link to its GitHub Repository → https://github.com/V-Squared/V-Squared.github.io. All code is contained in the index.html file.



## Dependencies
All scripts you need to load to make the Code Examples work:

### Angular
 ```
<script src="your/path/to/file/angular.min.js"></script>
```

### ngAnimate (if animation)

```
<script src="your/path/to/file/angular-animate.min.js"></script>
```

### v2Tooltip

```
<script src="your/path/to/file/v2Tooltip.js"></script>
```



## Example of SVG Element Tooltip
### Supports any closed SVG element including *Path*
Specifically: 

1. All SVG 1.1 Shapes (rect, cicrle, ellipse, line, polyline, polygon)
2. path (must be closed)

### SVG Element must have background fill
All SVG elements must be filled for the tooltip to work. The fill can be transparent.

### SVG Tooltip Code Example <a name="code-svg"></a>
```XML
<svg width="400" height="180">
  <rect x="50" y="20" width="150" height="150" fill-opacity="0" v2-tooltip="Hello" />
</svg>
```

## Example of Link in Tooltip <a name="link-in-tooltip"></a>
### Usage
The idea is very simple and practical. The Tooltip offer additional information to an element on the page. And in case the reader is interested in even more information at this time the → more ... link brings him directly to it.

### Implementation
Implementing it was hard when making it work intuitively with both big screen plus mouse and small screen with touch. In fact we could not find one tooltip plugin that could do it. This feature is why we coded v2-Tooltip. 

The challenge was to create a time out for removing the tooltip to allow for the mouse to leave the element that shows the tooltip and yet keep displaying it long enough to enter the tootip to keep it open, so that the user can navigate to the link and click it.

### Code example to turn on hover
This code is placed where you define your Angular Module

```Javascript
angular.module('yourApp', ['ngAnimate','v2.tooltip'], function(tooltipSettingsProvider) {
    tooltipSettingsProvider.options( {mouseoverTooltip: true} );
 })
```

### Link in Tooltip Code Example <a name="code-svg"></a>
```HTML
<g v2-tooltip="PC Know How & Tools.<br><a href=&quot;#for-diy&quot; du-smooth-scroll>For DIY</a>" transform="translate(14.247 -568.2)">
      <rect height="125" width="125" stroke="#000" y="568.79" x="111.43" fill="#fff"/>
      <text font-size="40px" xml:space="preserve" style="word-spacing:0px;letter-spacing:0px" y="635.93359" x="174.20323" font-family="sans-serif" line-height="125%" fill="#000000"><tspan y="635.93359" x="174.20323" font-size="15px" style="text-anchor:middle;text-align:center">DIY</tspan></text>
     </g>
```



# User Story of Tooltips making long content fun <a name="user-story"></a>
As an **Author of a Standard Web Site** I was faced with the conundrum to write short enough to not scare away the reader in the beginning yet long enough to satisfiy specilized needs. v2-Tooltip in combination with SVG Infographicsw solves this problem for us in a way I have described below:

## Conundrum of long, complex content
Our content is very complex. A typical reader is only interested in a small part of the content that we offer or respectively not interested in most of our content. Because our content is very networked, it is not possible to structure the content so that each reader can find all what he is interested grouped in one page. This created a conundrum in the past. If we made the page short enough to be attractive then the reader started reading, but left becuase we did not offered enough depth. Yet, when we offered enough depth, we could not capture the reader as it all was too long.

## Adventure Game Metaphor to the Rescue
Long content is not a problem if it is interesting to the reader. For our standard website [V²](http://v-squared.github.io) we use the Adventure Game Metaphyor to solve the above conundrum.

## Interactive Infographics to spice things up
A great infographics always catches the reader. Making it interactive with tooltips is even more fun. Now most of the content is hidden with tooltips, making the infographics clean. And what the reader is interested in he can uncover and explore via tooltips, like uncovering easter eggs. This way studying content becomes an adventure. The read more link in every tooltip makes it easy to follow the reading path of interest. Now the reader can keep reading what he is interested in while ignoring what he does not care about.

# Reference <a name="reference"></a>
- [v2-Tooltip Demo](http://v-squared.github.io/#delivering-puzzle)
   - [Features to Demo explained](#demo)
- [qtip2](http://qtip2.com/) Amazing jQuery Tooltip Plugin with an unbelievable number of features 
- [AngularJS](https://angularjs.org/) v2-Tooltip is written in AngularJS

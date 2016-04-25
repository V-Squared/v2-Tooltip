# v2-Tooltip
*SVG and HTML responsive Angular Tooltip Directive. Supports: Touch Screen, Mouse Over and Links and HTML in Tooltip.*


# Key Features
- **Lightweight:** Only 7 kB (not minimized) and minimum CPU load
- **Angular Directive:** 
- **SVG Support:** Easy to add Tooltips to SVG due to minimal code. See → [SVG Tooltip Code Example](#code-svg)
- **HTML Support:** 
- **Responsive:** 
- **Tablet Support:** 
- **Link in Tooltip:** 
- **Sanitized HTML in Tooltip:** 
- **Easy styling of Tooltip:** 


# Working Demo & Code
## Demo
- [Interactive Puzzle with Tooltips and Links](http://v-squared.github.io/#delivering-puzzle)
- **Open Tooltip**
   - **On PC:** Hover over puzzle to get Tooltip
   - **On Tablet:** Tab the Puzzle piece to get Tooltip
- **Using the Link:** 
   - **On PC:** Move mouse swiftly to hiver over tooltip. Then click link.
   - **On Tablet:** Tab the link in the Tooltip.
- **Responsive**
   - **Any Screeen Size:** Works on all screen sizes ranging from mobile phone to big screen
   - **Scaling support:** If SVG is bigger than screen size it scales down to fit. All Tooltip locations are scaled accordingly.
- **Show Selection:** 

# All Elements
## JavaScript
## CSS
## HTML
## Angular
## SVG
## Putting it all together

# Features in Detail
## SVG Support
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



# Reference
- [qtip2](http://qtip2.com/) Amazing jQuery Tooltip Plugin with an unbelievable number of features 

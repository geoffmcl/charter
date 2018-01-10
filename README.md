# CHARTER
A simple markdown **DSL** and **C Library** to generate svg plot from a minimal syntax.

## Example

Simple syntax example:

```
plot:
    y: 0, 2, 4, 9
    label: x^2
```

Resutls in:

<svg width="600" height="400">
<defs><clipPath id="plot-area"><rect x="52.50" y="25.00" width="512.00" height="350.00"/></clipPath></defs><line x1="75.77" y1="25.00" x2="75.77" y2="375.00" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="230.92" y1="25.00" x2="230.92" y2="375.00" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="386.08" y1="25.00" x2="386.08" y2="375.00" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="541.23" y1="25.00" x2="541.23" y2="375.00" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="52.50" y1="359.09" x2="564.50" y2="359.09" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="52.50" y1="288.38" x2="564.50" y2="288.38" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="52.50" y1="217.68" x2="564.50" y2="217.68" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="52.50" y1="146.97" x2="564.50" y2="146.97" style="stroke: #ccc;stroke-width:0.5"/>
<line x1="52.50" y1="76.26" x2="564.50" y2="76.26" style="stroke: #ccc;stroke-width:0.5"/>
<polyline points="75.77,359.09 230.92,288.38 386.08,217.68 541.23,40.91 " style="fill:none; stroke:#db5f57; stroke-width:2;" clip-path="url(#plot-area)"/>
<rect x="52" y="25" width="512" height="350" style="fill:none; stroke:black; stroke-width:0.5;" />
<line x1="75.77" y1="376.00" x2="75.77" y2="381.00" style="stroke: black;stroke-width:1"/>
<text x="75.77" y="395.00" text-anchor="middle">0</text>
<line x1="230.92" y1="376.00" x2="230.92" y2="381.00" style="stroke: black;stroke-width:1"/>
<text x="230.92" y="395.00" text-anchor="middle">1.0</text>
<line x1="386.08" y1="376.00" x2="386.08" y2="381.00" style="stroke: black;stroke-width:1"/>
<text x="386.08" y="395.00" text-anchor="middle">2.0</text>
<line x1="541.23" y1="376.00" x2="541.23" y2="381.00" style="stroke: black;stroke-width:1"/>
<text x="541.23" y="395.00" text-anchor="middle">3.0</text>
<line x1="46.50" y1="359.09" x2="51.50" y2="359.09" style="stroke: black;stroke-width:1"/>
<text x="42.50" y="359.09"  text-anchor="end" dy=".4em">0</text>
<line x1="46.50" y1="288.38" x2="51.50" y2="288.38" style="stroke: black;stroke-width:1"/>
<text x="42.50" y="288.38"  text-anchor="end" dy=".4em">2.0</text>
<line x1="46.50" y1="217.68" x2="51.50" y2="217.68" style="stroke: black;stroke-width:1"/>
<text x="42.50" y="217.68"  text-anchor="end" dy=".4em">4.0</text>
<line x1="46.50" y1="146.97" x2="51.50" y2="146.97" style="stroke: black;stroke-width:1"/>
<text x="42.50" y="146.97"  text-anchor="end" dy=".4em">6.0</text>
<line x1="46.50" y1="76.26" x2="51.50" y2="76.26" style="stroke: black;stroke-width:1"/>
<text x="42.50" y="76.26"  text-anchor="end" dy=".4em">8.0</text>
<rect x="454.50" y="35.00" width="100" height="21" style="fill:white; fill-opacity:0.5; stroke:#333; stroke-width:0.5;" />
<defs><clipPath id="leg-area"><rect x="494.50" y="35.00" width="58" height="21"/></clipPath></defs><line x1="464.50" y1="46.00" x2="494.50"  y2="46.00" style="fill:none; stroke:#db5f57; stroke-width:2;" /><text x="524.50" y="50.00" fill="#111" font-size="12" text-anchor="middle"  clip-path="url(#leg-area)">x\^2</text></svg>

## Syntax

| syntax | description |
| :----- | :------  |
|```plot```| create a new line plot|
|```x-axis```| parameters for the x axis |
|```y-axsi```| parameters for the y axis |
|```label``` | label for axis or plot |
|```x```| x values of a plot |
|```y```| y values of a plot | 
|```color```| colour of a plot |  
|```marker```| marker style of a plot ('o', 'x', '+', 's', ' ')|
|```range```| min and max value for an axis |
|```title```| plot title |
|```width```| plot width |
|```height```| plot height |
|```csv://file_path#tag```| load a csv and use column ```tag``` as values |

## Marker integration
At the moment _charter_ is integrated in [Marker](https://github.com/fabiocolacio/Marker/)!

![marker and charter](marker_charter_support.png)

## Credits

[csv_parser](https://github.com/JamesRamm/csv_parserhttps://github.com/JamesRamm/csv_parser) 
## Welcome to Blender-VRS Documentation


Using the addon includes 6 steps, distributed over 6 panels.

-------------

<a href="#curve-camber-alignment">Curve Camber Alignment</a>

<a href="#rig-creation">Rig Creation</a>

<a href="#curve-driver">Curve Driver</a>

<a href="#suspension">Suspension</a>

<a href="#binding-mesh-to-rig">Binding Mesh to Rig</a>

<a href="#tire-rotation">Tire Rotation</a>

-------------

<a href="#the-most-important-property-index">Index</a>

<a href="#detailed-suspension-properties">Detailed Suspension Properties</a>

-------------

<br/>
<br/>

### Curve Camber Alignment


![](/content/1.0.png)
</br>
`Camber Panel`

</br>

![](/content/1.1.png)
</br>
`First, select an index that was not used before in the scene, ignore it for the first time.`

</br>

![](/content/1.2.png)
</br>
`Second, enter wheelbase value by meters, see image above & below.`

<img src="/content/howto/1.2.png" width="314">

</br>
</br>

![](/content/1.3.png)
</br>
`Third, enter trackwidth value by meters, see image above & below.`

<img src="/content/howto/1.3.png" width="314">

</br>
</br>

![](/content/1.4.png)
</br>
`Fourth, select the curve and road surface.`

</br>

![](/content/1.5.png)
</br>
`Fifth, make sure the above properties are set properly, then click “Apply Camber”.`

</br>
</br>

### Rig Creation


![](/content/2.0.png)
</br>
`Rig Panel`

</br>

![](/content/2.1.png)
</br>
`Make sure the above properties are set properly, then click “Create Reader Rig”.`

</br>
</br>

### Curve Driver

![](/content/3.0.png)
</br>
`Driver Panel`

</br>

![](/content/3.1.png)
</br>
`First, enter lateral and longitudinal acceleration values, the larger the faster.`

<img src="/content/howto/3.12.gif" width="314">
<img src="/content/howto/3.11.gif" width="314">

</br>
</br>

![](/content/3.2.png)
</br>
`Second, enter slope effect ratio. Note: use values less than one if the road surface is steep, otherwise errors will show up.`

<img src="/content/howto/3.20.gif" width="314">

</br>
</br>

![](/content/3.3.png)
</br>
`Third, choose an initial frame, initial speed, final speed, and top speed.`

</br>

![](/content/3.4.png)
</br>
`Fourth, enter drifting slip angle, zero disables drifting. Then, enter the value in which how many skipped frames between keyframes for drift control.`

<img src="/content/howto/3.40.gif" width="314">

</br>
</br>

![](/content/3.5.png)
</br>
`Fifth, make sure the above properties are set properly, then click “Animate Curve Driver”.`

</br>
</br>

### Suspension

![](/content/4.0.png)
</br>
`Suspension Panel`

</br>

![](/content/4.1.png)
</br>
`First, three UI modes are depending on the level of customization the users want, basic is for me and most people, standard displays a reasonable number of properties, advanced is for nerds.`

</br>

![](/content/4.2.png)
</br>
`Second, presets are pre-set or preset, it's somewhat obvious, 5 modes are included depending on the final desired look.`

<img src="/content/howto/3.40.gif" width="314">

</br>
</br>

![](/content/4.3.png)
</br>
`Third, Independent Suspension Properties will allow you to tune each wheel suspension independently of other wheels. Note: this option is experimental, not insured to produce professional results.`

</br>

![](/content/4.4.png)
</br>
`Fourth, set the start frame and end frame, the longer the interval the longer the processing time. Then, set the sub-frames, usually set at 100, doesn’t affect the processing time as much as the frame’s interval. Note: make sure that your scene can play the animation at a decent frame rate, this can hugely impact processing time for no reason, best way to speed it up is by hiding unnecessary objects and applying modifiers so that it doesn’t compute modifiers every frame change.`

</br>

![](/content/4.5.png)
</br>
`Note: Detailed suspension properties are explained at the end of the documentation.`

<a href="#detailed-suspension-properties">Detailed Suspension Properties</a>

</br>

![](/content/4.6.png)
</br>
`Fifth, make sure the above properties are set properly, then click “Animate Suspension”. Note: “Animate Suspension” is the only operator in the addon that you can click more than once per index, this is so that you can check the suspension results and redo them whenever you want.`

</br>
</br>

### Binding Mesh to Rig

![](/content/5.0.png)
</br>
`Before choosing your parts, binding requires a simple procedure.`

</br>
</br>

<img src="/content/howto/5.1.png" width="628"></br>`First, make sure your rear axle is sitting above the centre of the world, and the car front facing the positive x-axis.`

</br>

<img src="/content/howto/5.20.png" width="628"></br>`Second, follow the following diagram on how you are required to parent the tires and brakes to the car base (Arrows point towards parent).`

</br>

<img src="/content/howto/5.21.png" width="628"></br>`Note: for complex models that have more than one object such as separated wheel and tire, etc. parent all these objects to the tire and select the tire in the add-on UI. As shown above.`

</br>
</br>

![](/content/5.1.png)
</br>
`Third, choose the tires, the car base, and the brake object.`

<img src="/content/howto/5.22.gif" width="628">

</br>
</br>

![](/content/5.2.png)
</br>
`Fourth, make sure the above properties are set properly, then click “Bind”.`

</br>
</br>

### Tire Rotation

![](/content/6.0.png)
</br>
`Tire Rotation Panel`

</br>

![](/content/6.1.png)
</br>
`Make sure the index is set properly, then click “Apply Rotation”.`

</br>

**Note: If you did not use mesh as your tires in the “Binding Mesh to Rig” tab, you must enter tires diameter manually.**

![](/content/6N.1.png)

<img src="/content/howto/6.1.png" width="314">

</br>

--------------


### The most important property, “Index”

### Detailed Suspension Properties









------------------------------------------------------------------------------------------------------------------


You can use the [editor on GitHub](https://github.com/32OO2/VRS.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/32OO2/VRS.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

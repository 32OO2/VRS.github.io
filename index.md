## Welcome to Blender-VRS Documentation


Using the addon includes 6 steps, distributed over 6 panels.

-------------

<a href="#curve-camber-alignment">1 - Curve Camber Alignment</a>

<a href="#rig-creation">2 - Rig Creation</a>

<a href="#curve-driver">3 - Curve Driver</a>

<a href="#suspension">4 - Suspension</a>

<a href="#binding-mesh-to-rig">5 - Binding Mesh to Rig</a>

<a href="#tire-rotation">6 - Tire Rotation</a>

-------------

<a href="#the-most-important-property-index">Index</a>

<a href="#detailed-suspension-properties">Detailed Suspension Properties</a>

-------------

<br/>
<br/>

### Curve Camber Alignment


![](/content/1.0.png)
<br/>
`Camber Panel`

<br/>

![](/content/1.1.png)
<br/>
`First, select an index that was not used before in the scene, ignore it for the first time.`

<br/>

![](/content/1.2.png)
<br/>
`Second, enter wheelbase value by meters, see image above & below.`

<img src="/content/howto/1.2.png" width="314">

<br/>
<br/>

![](/content/1.3.png)
<br/>
`Third, enter trackwidth value by meters, see image above & below.`

<img src="/content/howto/1.3.png" width="314">

<br/>
<br/>

![](/content/1.4.png)
<br/>
`Fourth, select the curve and road surface.`

<br/>

![](/content/1.5.png)
<br/>
`Fifth, make sure the above properties are set properly, then click “Apply Camber”.`

<br/>
<br/>

### Rig Creation


![](/content/2.0.png)
<br/>
`Rig Panel`

<br/>

![](/content/2.1.png)
<br/>
`Make sure the above properties are set properly, then click “Create Reader Rig”.`

<br/>
<br/>

### Curve Driver

![](/content/3.0.png)
<br/>
`Driver Panel`

<br/>

![](/content/3.1.png)
<br/>
`First, enter lateral and longitudinal acceleration values, the larger the faster.`

<img src="/content/howto/3.12.gif" width="314">
<img src="/content/howto/3.11.gif" width="314">

<br/>
<br/>

![](/content/3.2.png)
<br/>
`Second, enter slope effect ratio. Note: use values less than one if the road surface is steep, otherwise errors will show up.`

<img src="/content/howto/3.20.gif" width="314">

<br/>
<br/>

![](/content/3.3.png)
<br/>
`Third, choose an initial frame, initial speed, final speed, and top speed.`

<br/>

![](/content/3.4.png)
<br/>
`Fourth, enter drifting slip angle, zero disables drifting. Then, enter the value in which how many skipped frames between keyframes for drift control.`

<img src="/content/howto/3.40.gif" width="314">

<br/>
<br/>

![](/content/3.5.png)
<br/>
`Fifth, make sure the above properties are set properly, then click “Animate Curve Driver”.`

<br/>
<br/>

### Suspension

![](/content/4.0.png)
<br/>
`Suspension Panel`

<br/>

![](/content/4.1.png)
<br/>
`First, three UI modes are depending on the level of customization the users want, basic is for me and most people, standard displays a reasonable number of properties, advanced is for nerds.`

<br/>

![](/content/4.2.png)
<br/>
`Second, presets are pre-set or preset, it's somewhat obvious, 5 modes are included depending on the final desired look.`

<img src="/content/howto/3.40.gif" width="314">

<br/>
<br/>

![](/content/4.3.png)
<br/>
`Third, Independent Suspension Properties will allow you to tune each wheel suspension independently of other wheels. Note: this option is experimental, not insured to produce professional results.`

<br/>

![](/content/4.4.png)
<br/>
`Fourth, set the start frame and end frame, the longer the interval the longer the processing time. Then, set the sub-frames, usually set at 100, doesn’t affect the processing time as much as the frame’s interval. Note: make sure that your scene can play the animation at a decent frame rate, this can hugely impact processing time for no reason, best way to speed it up is by hiding unnecessary objects and applying modifiers so that it doesn’t compute modifiers every frame change.`

<br/>

![](/content/4.5.png)
<br/>
`Note: Detailed suspension properties are explained at the end of the documentation.`

<a href="#detailed-suspension-properties">Detailed Suspension Properties</a>

<br/>

![](/content/4.6.png)
<br/>
`Fifth, make sure the above properties are set properly, then click “Animate Suspension”. Note: “Animate Suspension” is the only operator in the addon that you can click more than once per index, this is so that you can check the suspension results and redo them whenever you want.`

<br/>
<br/>

### Binding Mesh to Rig

![](/content/5.0.png)
<br/>
`Before choosing your parts, binding requires a simple procedure.`

<br/>
<br/>

<img src="/content/howto/5.1.png" width="628"><br/>`First, make sure your rear axle is sitting above the centre of the world, and the car front facing the positive x-axis.`

<br/>

<img src="/content/howto/5.20.png" width="628"><br/>`Second, follow the following diagram on how you are required to parent the tires and brakes to the car base (Arrows point towards parent).`

<br/>

<img src="/content/howto/5.21.png" width="628"><br/>`Note: for complex models that have more than one object such as separated wheel and tire, etc. parent all these objects to the tire and select the tire in the add-on UI. As shown above.`

<br/>
<br/>

![](/content/5.1.png)
<br/>
`Third, choose the tires, the car base, and the brake object.`

<img src="/content/howto/5.22.gif" width="628">

<br/>
<br/>

![](/content/5.2.png)
<br/>
`Fourth, make sure the above properties are set properly, then click “Bind”.`

<br/>
<br/>

### Tire Rotation

![](/content/6.0.png)
<br/>
`Tire Rotation Panel`

<br/>

![](/content/6.1.png)
<br/>
`Make sure the index is set properly, then click “Apply Rotation”.`

<br/>

**Note: If you did not use mesh as your tires in the “Binding Mesh to Rig” tab, you must enter tires diameter manually.**

![](/content/6N.1.png)

<img src="/content/howto/6.1.png" width="314">

<br/>

--------------


### The most important property, “Index”

The index is a numerical identifier used so that VRS can be used for multiple vehicles in the same scene. just check the index before you press any processing button, and the process will occur for the rig with that index.

![](/content/Index.png)

--------------

### Detailed Suspension Properties

![](/content/susp/7.0.png)
<br/>
`Suspension Panel`

![](/content/susp/7.1.png)
<br/>
`Spring Stiffness: Spring rate, the higher the faster the spring oscillate lower values represents softer and slower spring, higher values represent stiffer and faster spring.`
<br/>
<img src="/content/suspprops/SuspStiffness.gif" width="618">

<br/>
<br/>


![](/content/susp/7.2.png)
<br/>
`Suspension Damping: the higher the less oscillation the vehicle does before resting, should be set regarding spring stiffness (the higher the stiffness the higher the damping should be), higher values represent vehicles with less swinging (luxury vehicles), lower values represent vehicles with more swinging (essential for cartoonish look).`

**Tip: for realistic visuals, set damping value so that the vehicle does not oscillate more than twice before resting.**
<br/>
<img src="/content/suspprops/SuspDamping.gif" width="618">

<br/>
<br/>


![](/content/susp/7.3.png)
<br/>
`Suspension Travel: the length of the spring, the higher the longer the vertical distance the tires can encounter.`
<br/>
<img src="/content/suspprops/SuspTravel.png" width="618">

<br/>
<br/>


![](/content/susp/7.4.png)
<br/>
`Spring Preload: the distance that the spring is compressed at full extension of the suspension. For a suspension Travel of 0.5m and Spring Preload of 0.1m, a 0.6m long spring is used and allowed to only expand 0.5m.`
<br/>
<img src="/content/suspprops/SuspPreload.png" width="618">

<br/>
<br/>


![](/content/susp/7.5.png)
<br/>
`Spring Min Height: the minimum length the spring can be compressed at.`
<br/>
<img src="/content/suspprops/SuspMinH.png" width="618">

<br/>
<br/>


![](/content/susp/7.6.png)
<br/>
`Tire Stiffness: Tires in VRS is simulated as if it is a spring, therefore: is similar to how suspension spring stiffness works, but for the tire. Also, stiffer and higher values are used here, since smaller travel is allowed.`

<br/>

![](/content/susp/7.7.png)
<br/>
`Tire Damping: As above.`
<br/>
**Tip: Use high values for Tire Damping since it naturally stabilizes the motion.**

<br/>

![](/content/susp/7.8.png)
<br/>
`Tire Rest Height: tire spring length, similar to Suspension travel, but for the tire.`

<br/>

![](/content/susp/7.9.png)
<br/>
`Tire Min Height: the minimum length the tire spring can be compressed at. similar to Suspension Min Height, but for the tire.`

<br/>

![](/content/susp/7.10.png)
<br/>
`Wheel Base Multiplier: this property allows to control the body lean to front and rear. The more it is the more body lean will occur.`

<br/>

![](/content/susp/7.11.png)
<br/>
`Track Width Multiplier: this property allows to control the body lean from side to side. The more it is the more body lean will occur.`
<br/>
**Note, if the simulation shows inappropriate results such as the car disappearing, then this means the car will experience rollover. decrease these above multipliers to fix the issue.**

<br/>

![](/content/susp/7.12.png)
<br/>
`Vehicle mass: the mass, by Kg, the higher the softer the springs and dampers will act like.`

<br/>

![](/content/susp/7.13.png)
<br/>
`Center of mass Height: how high the centre of mass is from the ground, don’t use values higher than half the wheelbase or track width, or the vehicle may encounter rollover.`

<br/>

![](/content/susp/7.14.png)
<br/>
`Gravity: tweaking the gravity allows for fewer or more jumps. If your car is jumping too much, then use a stronger gravity value and vice versa. Note: always negative, positive values will slowly send the vehicle to the sky.`

<br/>

![](/content/susp/7.15.png)
<br/>
`Unsprung mass: mass of suspension parts for each tire. (Parts that are connecting the tire to the Coilover)`

<br/>

![](/content/susp/7.16.png)
<br/>
`Wheel Mass: Mass of each wheel including the tire.`

<br/>

![](/content/susp/7.17.png)
<br/>
`Error Clamper: higher values give less tolerance but can cause errors. Lower values can cause more tolerances and may trigger false error reports.`

<br/>

### THE END
#### that was a long list!
#### Thanks For Reading!!!

<a href="#welcome-to-blender-vrs-documentation">Go to Top</a>

<a href="https://3200z.gumroad.com/l/xcCDiu">Get Blender-VRS</a>

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>

# 360-246-assignment-2-velocity-fields-solved
**TO GET THIS SOLUTION VISIT:** [360.246 Assignment 2-Velocity Fields Solved](https://www.ankitcodinghub.com/product/360-246-assignment-2-velocity-fields-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100603&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;360.246 Assignment 2-Velocity Fields Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
<div class="column">
You may use any compiler of your liking, however we recommend additional warning output. When using GCC, at least the following flags should be set: -std=c++11 -Wall -Wextra -pedantic

Make sure you structure your programs in a readable fashion. It will make you more efficient and help us identify possible errors easily, i.e.: save you marks if there are problems.

This exercise requires you to use the library ViennaLS. Install instructions for C++ and Python modules are available at https://github.com/ViennaTools/ViennaLS.

ViennaLS Basics

</div>
</div>
<div class="layoutArea">
<div class="column">
In order to get acquainted with the level set library ViennaLS, we will first cover some basics. We want to rebuild the snowman example from https://github.com/ViennaTools/viennals-example. You can follow the source file Frosty.cpp for reference in the following sections.

1.1 A Sphere / Snowball

The journey of a thousand snowmen starts with a single snowball.

<ul>
<li>The first thing we need, is space to put a level set into. The simulation domain is represented by lsDomain. If nothing is passed to the class upon construction, the grid delta is 1.0 and there are no boundary conditions, because the domain is infinite and will extend as far the surface reaches.</li>
<li>Now we need to put some surface into the domain. This is done using lsMakeGeometry. The Documenta- tion contains all the shapes that can be created with this class. For simplicity, start with a sphere centred at the origin.</li>
<li>Now use lsToSurfaceMesh to extract a surface from the level set. The resulting lsMesh object can then be written to a VTK file using the lsVTKWriter.</li>
<li>In order to view the grid points of the level set and their level set values, use lsToMesh and compare it with the explicit surface. Notice that ViennaLS uses a sparse level set representation.</li>
<li>Inspect your first level set sphere using ParaView.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
1.2 Melting a Sphere

In order to simulate the melting of our sphere, we need to advect the level set:

• The class lsAdvect performs the advection for us. It needs all level sets which are involved in the advection

and a class inherited from lsVelocityField, which describes the velocity field by which to advect. • The best way to pass lsDomains to lsAdvect is using insertNextLevelSet:

<pre>     lsAdvect&lt;double, D&gt; advectionKernel();
     advectionKernel.insertNextLevelSet(myLsDomain);
</pre>
• Now we just need a velocity field. The simplest velocity field, just returns a constant: class velocityField : public lsVelocityField&lt;double&gt; {

</div>
</div>
<div class="layoutArea">
<div class="column">
public :

</div>
</div>
<div class="layoutArea">
<div class="column">
} };

</div>
</div>
<div class="layoutArea">
<div class="column">
double

</div>
<div class="column">
getScalarVelocity (

const std : : array&lt;double , 3&gt; &amp; /∗ coordinate ∗/ , int /∗material∗/,

const std : : array&lt;double , 3&gt; &amp;/∗normalVector ∗/ , unsigned long /∗pointID∗/) final {

return −1;

</div>
</div>
<div class="layoutArea">
<div class="column">
The above implementation means, that the velocity is -1 at every point on the surface, therefore our snowman is melting in the sun.

• A single apply call performs one advection step adhering to the CFL condition. If the physical advection time was set by setAdvectionTime(), several steps will be taken until the given time in seconds has passed. In the Example, this results in the surface shown in Fig. 1.

Figure 1: Evolution of the snowman level set by ”melting” the snowman for 1 second.

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
1.3 Multiple Materials

Snowmen consist of multiple spheres, as shown in Frosty.cpp.

<ul>
<li>In order to get stable numerics, layer wrapping is used during advection. In order to combine two level
sets for a wrapped layer including both, lsBooleanOperation is used.
</li>
<li>During advection, only one level set can be moved at a time, the ”top” level set. However, the wrapping approach makes it possible to include ”lower” materials. If several level sets have the same level set value at the same point in space, the velocity for the ”lowest” level set is taken, as shown in Fig. 2. Lower level sets are adjusted to the top level set after etching. During deposition, lower level sets do not change. See the lsAdvect Documentation for details.</li>
<li>The different velocities can be set in the velocity field. See Frosty.cpp for reference.
Figure 2: Multiple wrapped materials on the sidewall of a trench geometry. The coloured lines show the location of the explicit surface. Red includes green which includes blue. At the grid point A, the velocity of blue is applied, because it is the lowest layer present at that point. At grid point B it is green, and at C red.
</li>
</ul>
2 Emulating a Real Process

The possibility to set a velocity field for different materials is already quite powerful in creating semiconductor structures. Now we can use one level set as a mask by setting its velocity to something very small (or 0).

2.1 Via Etch

Deep vias are usually fabricated by a series of different etch and deposition steps, known as deep reactive-ion etching (DRIE) or the Bosch Process:

<ul>
<li>First, isotropic deposition of a passivating material protects all parts of the substrate.</li>
<li>Etching of the passivating layer and the substrate takes place. This is almost perfectly directional for the passivating layer because it is mostly removed by high energy ions. For the substrate it is almost isotropic since the substrate is removed mostly chemically.
This process can be emulated, by considering only the velocities on the surface. The result should look similar to Fig. 3.

2.2 Task
</li>
</ul>
<ul>
<li>Create a three-dimensional simulation domain with two reflective boundaries and one infinite boundary. You can choose the size and grid spacing as you want, however we recommend a grid extent of [−40μm, 40μm] in the x- and y-directions and a grid spacing of 1μm.</li>
<li>Starting from a single plane (substrate/silicon) with normal towards the infinite boundary, deposit a mask material on top.</li>
<li>Use Boolean operations to generate a circular hole in the mask, but not in the substrate. Since the process will only be active in exposed parts of the substrate, the hole in the mask should span most of the simulation domain. (Hint: Use lsMakeGeometry using an lsCylinder to make a cylinder.)</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Figure 3: Schematic of a cycle of DRIE.

<ul>
<li>Emulate several cycles of the Bosch process to create a deep hole in the substrate. Assume perfectly isotropic deposition and perfectly directional etching for the passivation layer. Assume perfectly isotropic etching of the substrate. Be aware that deposition creates a third material, not silicon or mask, so it will need different velocities than the other two! Describe in your report, which deposition/etch rates and distributions lead to satisfactory results.</li>
<li>Evaluate how increasing/decreasing the cycle times changes the profile. How does the sidewall roughness (horizontal deviation) change? How deep is the etched hole per cycle in relation to the used rates? What is the benefit/drawback of using longer but fewer cycles?</li>
<li>Try changing the etch process to be more isotropic instead of perfectly directional. How does the distri- bution of the etch process (more isotropic versus more directional) influence the final structure?</li>
<li>What properties of the process influence the size of a single scallop in the sidewall and how?</li>
<li>Present your results in your report, including figures of the final structures, making sure you include
necessary information, such as dimensions and axis labels.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
3 Creating Transistor Structures

In the above Task, you have created a single via through a silicon substrate. Although it is a complex process with many steps, it does not look particularly thrilling. Now, we want to create a full transistor using just a chain of simple addition/removal steps. During actual fabrication several complex processing techniques are required, such as sophisticated plasma etching for directional etch steps, which we will try to mimic using simple velocity profiles. Chemical Mechanical Planarization (CMP) is commonly used to flatten the top of structures. CMP should be approximated by simply defining a flat plane and removing material above it using Boolean operations.

3.1 FinFET Transistor

FinFET transistors have a ”fin” connecting the source and drain, which is raised above the substrate, as shown in Fig. 4. Such a raised conductive channel leads to an improved electrical response in the transistor channel.

Figure 4: Schematic of a single FinFET on an insulating oxide layer. The insulating spacer between channel and gate is shown in yellow, Silicon is shown in grey and the gate is shown in green.

3.2 Task

Build a FinFET structure using the deposition/etch steps listed in Table 1, which will lead to the structure shown in Fig. 4. Be sure to wrap the level set layers correctly to advect the top level set as expected. Mask layers should not be simulated here, but are assumed to be perfect boxes on top of the material (Hint: Create them with Boolean operations). Work in units of nanometers for easier calculations and fewer rounding errors.

</div>
</div>
<div class="layoutArea">
<div class="column">
Process Oxide Deposition Silicon Deposition Mask Creation Fin Creation Mask Removal Spacer Deposition Gate Deposition Gate CMP Gate Mask Gate Patterning Mask Removal

</div>
<div class="column">
Properties

Start from a single 200x200nm plane (this is the Oxide).

Deposit 50nm of Silicon

Create a mask (a box) on top of the silicon with 20nm width. Directional Etch of Silicon down to the Oxide

Simply delete the Mask level set

Isotropic deposition of 5nm of Spacer (yellow in Fig. 4) everywhere Deposit 80nm of Gate Material everywhere

Use a plane 70nm above the Oxide to flatten the Gate Material

Add a 10nm wide mask (box) perpendicular to the fin on top of the Gate Etch Gate and Spacer directionally, resulting in a 10nm wide Gate Delete the Mask material

</div>
</div>
<div class="layoutArea">
<div class="column">
Table 1: Process Sequence for the creation of a silicon fin and gate.

• Generate a FinFET structure using the process steps in Table 1 In your first simulation assume etching is perfectly directional and deposition is perfectly isotropic. In your report, include the parameters you have used and describe how each of them influences the result.

</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
<ul>
<li>Introduce some isotropy to the directional processes. How does it affect the final structure?</li>
<li>What happens when directional etch processes (Fin creation, Spacer Etch and Gate Patterning) have
positive isotropic components? Can you think of a process which can achieve this?
</li>
<li>On the edges of wafers, the plasma of plasma etch steps may not be perfectly uniform. Try changing the direction of the directional processes to be slightly skewed. What happens?</li>
<li>The simple Engquist-Osher advection scheme, we have discussed is often not enough to describe directional etch steps sufficiently. Try changing your advection scheme to the more sophisticated Lax-Friedrichs scheme for the directional etch steps. Usually, this integration scheme, would need calibration to the specific process, however the default settings work well for V = n⃗z, so a simple directional etch. Hint: This can be done by using
lsAdvect::setIntegrationScheme(lsIntegrationSchemeEnum::LAX FRIEDRICHS 1ST ORDER)
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>

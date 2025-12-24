<h1>Stability Circles on the Smith Chart</h1>

<p>
This document explains how to write the <b>stability circle equations</b>
in the same <b>center–radius form</b> used for Smith chart circles.
</p>

<hr>

<h2>1. Smith Chart Circle Form</h2>

<p>
Let the reflection coefficient be:
</p>

<p>
<b>&Gamma; = r + j i</b>
</p>

<p>
The general equation of a circle in the Smith chart plane is:
</p>

<p>
<b>(r − r<sub>0</sub>)<sup>2</sup> + (i − i<sub>0</sub>)<sup>2</sup> = R<sup>2</sup></b>
</p>

<p>
Example (constant reactance circle):
</p>

<p>
<b>
(r − 1)<sup>2</sup> + (i − 1/x<sub>L</sub>)<sup>2</sup> = (1/x<sub>L</sub>)<sup>2</sup>
</b>
</p>

<hr>

<h2>2. Stability Circles Are Also Circles</h2>

<p>
Input and output stability circles are <b>circles in the reflection coefficient plane</b>.
They use the same mathematical form:
</p>

<p>
<b>
(r − Re{C})<sup>2</sup> + (i − Im{C})<sup>2</sup> = R<sup>2</sup>
</b>
</p>

<hr>

<h2>3. Output (Load) Stability Circle</h2>

<h3>Center</h3>

<p>
<b>
C<sub>L</sub> =
&frac12;
(S<sub>22</sub> − &Delta; S<sub>11</sub><sup>*</sup>)<sup>*</sup>
/
(|S<sub>22</sub>|<sup>2</sup> − |&Delta;|<sup>2</sup>)
</b>
</p>

<h3>Radius</h3>

<p>
<b>
R<sub>L</sub> =
|
S<sub>12</sub>S<sub>21</sub>
/
(|S<sub>22</sub>|<sup>2</sup> − |&Delta;|<sup>2</sup>)
|
</b>
</p>

<h3>Circle Equation</h3>

<p>
Let <b>&Gamma;<sub>L</sub> = r + j i</b>, then:
</p>

<p>
<b>
(r − Re{C<sub>L</sub>})<sup>2</sup> + (i − Im{C<sub>L</sub>})<sup>2</sup> = R<sub>L</sub><sup>2</sup>
</b>
</p>

<hr>

<h2>4. Input (Source) Stability Circle</h2>

<h3>Center</h3>

<p>
<b>
C<sub>S</sub> =
&frac12;
(S<sub>11</sub> − &Delta; S<sub>22</sub><sup>*</sup>)<sup>*</sup>
/
(|S<sub>11</sub>|<sup>2</sup> − |&Delta;|<sup>2</sup>)
</b>
</p>

<h3>Radius</h3>

<p>
<b>
R<sub>S</sub> =
|
S<sub>12</sub>S<sub>21</sub>
/
(|S<sub>11</sub>|<sup>2</sup> − |&Delta;|<sup>2</sup>)
|
</b>
</p>

<h3>Circle Equation</h3>

<p>
Let <b>&Gamma;<sub>S</sub> = r + j i</b>, then:
</p>

<p>
<b>
(r − Re{C<sub>S</sub>})<sup>2</sup> + (i − Im{C<sub>S</sub>})<sup>2</sup> = R<sub>S</sub><sup>2</sup>
</b>
</p>

<hr>

<h2>5. Key Notes</h2>

<ul>
  <li>Stability circles are frequency dependent</li>
  <li>They are plotted on the Smith chart using center and radius</li>
  <li>The equations define only the circle, not the stable side</li>
  <li>The stable region is found by testing a point (usually &Gamma; = 0)</li>
</ul>

<hr>

<p>
<b>Conclusion:</b>  
Stability circles use the same mathematical form as Smith chart circles; only the
center and radius are determined from S-parameters.
</p>


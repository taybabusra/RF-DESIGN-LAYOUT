✅ 1. “Field Theory for RF Engineers” — ONE-PAGE CHEAT SHEET

This gives you exactly the amount of field theory needed for RF/Microwave work.

⭐ A. Maxwell’s Equations (Engineering Form)
1️⃣ Faraday’s Law
∇
×
𝐸
=
−
𝑗
𝜔
𝐵
∇×E=−jωB

Changing magnetic field → induces voltage.

2️⃣ Ampere–Maxwell Law
∇
×
𝐻
=
𝑗
𝜔
𝐷
+
𝐽
∇×H=jωD+J

Changing electric field → creates magnetic field.

3️⃣ Gauss’s Law (Electric)
∇
⋅
𝐷
=
𝜌
∇⋅D=ρ
4️⃣ Gauss’s Law (Magnetic)
∇
⋅
𝐵
=
0
∇⋅B=0

(No magnetic monopoles.)

⭐ B. Constitutive Relations
𝐷
=
𝜀
𝐸
D=εE
𝐵
=
𝜇
𝐻
B=μH
𝐽
=
𝜎
𝐸
J=σE

Loss tangent:

tan
⁡
𝛿
=
𝜎
+
𝜔
𝜀
′
′
𝜔
𝜀
′
tanδ=
ωε
′
σ+ωε
′′
	​

⭐ C. Boundary Conditions

At any material interface:

Tangential E is continuous:

𝐸
1
𝑡
=
𝐸
2
𝑡
E
1t
	​

=E
2t
	​


Tangential H jumps with surface current:

𝐻
1
𝑡
−
𝐻
2
𝑡
=
𝐽
𝑠
H
1t
	​

−H
2t
	​

=J
s
	​


Normal D jumps with surface charge:

𝐷
2
𝑛
−
𝐷
1
𝑛
=
𝜌
𝑠
D
2n
	​

−D
1n
	​

=ρ
s
	​


Normal B continuous:

𝐵
1
𝑛
=
𝐵
2
𝑛
B
1n
	​

=B
2n
	​

⭐ D. Wave Equation
∇
2
𝐸
+
𝑘
2
𝐸
=
0
∇
2
E+k
2
E=0

Propagation constant:

𝛾
=
𝛼
+
𝑗
𝛽
γ=α+jβ

Lossless:

𝛾
=
𝑗
𝛽
,
𝛽
=
2
𝜋
𝜆
γ=jβ,β=
λ
2π
	​

⭐ E. Plane Waves
𝐸
(
𝑧
)
=
𝐸
0
𝑒
−
𝛾
𝑧
E(z)=E
0
	​

e
−γz

Wave impedance:

𝜂
=
𝜇
𝜀
η=
ε
μ
	​

	​

⭐ F. Power Flow (Poynting Vector)
𝑆
=
𝐸
×
𝐻
S=E×H
𝑃
avg
=
1
2
ℜ
(
𝐸
𝐻
∗
)
P
avg
	​

=
2
1
	​

ℜ(EH
∗
)
⭐ G. Reflection/Transmission

Reflection coefficient:

Γ
=
𝑍
𝐿
−
𝑍
0
𝑍
𝐿
+
𝑍
0
Γ=
Z
L
	​

+Z
0
	​

Z
L
	​

−Z
0
	​

	​


Standing-wave ratio:

VSWR
=
1
+
∣
Γ
∣
1
−
∣
Γ
∣
VSWR=
1−∣Γ∣
1+∣Γ∣
	​

⭐ H. Modes (TEM / TE / TM)

TEM: both E and H have no “z-component” → coax, microstrip.

TE: Ez = 0 → rectangular waveguide.

TM: Hz = 0 → some waveguide modes.

🔥 This is the exact level of field theory needed for RF.
✅ 2. Complete Roadmap — “Field Theory Needed for Microwave Engineering”

This tells you exactly how deep you need to go, chapter by chapter.

⭐ LEVEL 1 — Must Know (Core RF Foundation)

These are non-negotiable:

Maxwell’s equations (conceptually)

Boundary conditions

Wave equation

Plane waves

Wave impedance

Reflection & transmission coefficients

Skin depth

Poynting vector

TE/TM/TEM modes

Cutoff frequency in waveguides

Radiation basics

⭐ LEVEL 2 — Useful for Advanced RF

You should know these if you’re doing RF design:

Field distribution in waveguides

Field distribution in microstrip/stripline

Resonator field shapes

Cavity Q factor from fields

Image theory (antennas)

Reciprocity theorem

Near-field vs far-field regions

⭐ LEVEL 3 — Optional (Only for R&D / HFSS / CST Work)

You do not need these for most RF jobs:

Full solutions to Maxwell’s equations in cylindrical/spherical coordinates

Green’s functions

Stratton–Chu formulas

Dyadic fields

Tensor permittivity/permeability

Numerical solvers (FDTD, FEM) theory

⭐ LEVEL 4 — Not Needed for RF at All

(Unless you're doing theoretical physics)

Quantum field theory

Gauge theory

Relativistic electrodynamics

Magnetic monopole theory

Quantum electrodynamics (QED)

🎯 Summary of What YOU Must Learn for RF

You need enough field theory to:

Understand transmission lines

Understand waveguides

Understand antennas

Understand impedance matching

Understand reflections & scattering parameters

Everything else is optional.

✅ 3. “10 Super Intuitive Maxwell’s Equations Explanations”

These are the best intuitive interpretations for RF engineers.

1️⃣ Gauss’s Law for E: Charges create electric field.

If you put charge somewhere → E-field radiates out.

2️⃣ Gauss’s Law for B: No magnetic charge exists.

There are no magnetic “monopoles,” so magnetic flux loops.

3️⃣ Faraday’s Law: Changing magnetic field makes voltage.

This is how inductors and generators work.

4️⃣ Ampere–Maxwell Law: Changing electric field makes magnetic field.

This is how antennas radiate.

5️⃣ Waves happen because E and H keep generating each other.

An EM wave is a “self-sustaining dance” between E and H fields.

6️⃣ Boundary conditions = field behavior at surfaces.

Like water flow hitting walls, fields behave differently at interfaces.

7️⃣ Reflection coefficient is field mismatch at boundary.

Reflection occurs when wave impedance does not match.

8️⃣ Skin depth = AC currents stay on the surface.

At RF, current hugs the surface → copper plating matters.

9️⃣ Wave impedance is the E/H ratio of a wave.

It determines how much of the wave reflects or transmits.

🔟 Poynting vector = direction of power flow.
𝑆
=
𝐸
×
𝐻
S=E×H

Power always flows perpendicular to both E and H.

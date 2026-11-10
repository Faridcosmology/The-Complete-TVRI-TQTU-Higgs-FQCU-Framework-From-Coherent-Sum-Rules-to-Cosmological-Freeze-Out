# The-Complete-TVRI-TQTU-Higgs-FQCU-Framework-From-Coherent-Sum-Rules-to-Cosmological-Freeze-Out
MONOGRAPH E1
The Complete TVRI–TQTU Higgs–FQCU Framework: From Coherent Sum Rules to Cosmological Freeze-Out

Author: Prof. Dr. Md. Faridul Islam Chowdhury, MBBS, DA, MS (Neurosurgery)
Affiliation: Founder & Director, Tanfarid Vision Research Institute (TVRI), Bogura, Bangladesh
ORCID: 0000-0003-3178-0671
Document ID: TVRI-TQTU-2026-MONOGRAPH-E1
Status: Complete Monograph — Submission Ready
Target: Physics Reports / Springer Lecture Notes in Physics
Front Matter
Preface

This monograph consolidates eleven journal articles — themselves derived from twenty-four sequential research sections — into a unified account of the Higgs–FQCU Coherent Three-Scalar Framework developed within the Tanfarid Quantum Thermodynamic Universe (TQTU) program at the Tanfarid Vision Research Institute (TVRI). The work spans the construction of the coherent propagator, the derivation of an exact interference sum rule, the numerical integration of the thermal collision network, the design of a mass-consistent conservative Boltzmann solver, and the analysis of the entropy-driven approach to chemical equilibrium.

Throughout, the reader will find a consistent scientific methodology: every claim is either derived analytically, verified numerically, or explicitly labeled as conditional. Where the current state of the calculation does not support a physical conclusion, that limitation is stated. This is the spirit in which the work is offered — not as a claim of discovery, but as a falsifiable theoretical program with documented numerical evidence.
Abstract

We present the complete theoretical and computational framework of the Higgs–FQCU Coherent Three-Scalar model. The model couples a Standard Model-like Higgs sector to an ultra-light angular scalar of mass ma=4.135667696 meVma​=4.135667696 meV through three CP-even mass eigenstates (m1=125.09 GeVm1​=125.09 GeV, m2=500 GeVm2​=500 GeV, m3=1006.61 GeVm3​=1006.61 GeV). The three-mediator coherent propagator obeys an exact partial-fraction identity, ∑iRi/mi2=0∑i​Ri​/mi2​=0, which eliminates the low-energy contact term and produces an annihilation cross-section scaling as σffˉ→aa∝mf2s2σffˉ​→aa​∝mf2​s2. We systematically develop: (i) the algebraic structure of the sum rule and its implications for fermionic thermal rates; (ii) a resonance-safe collision solver architecture; (iii) a mass-consistent, conservative quantum Boltzmann solver with exact detailed-balance preservation; (iv) numerical consistency tests including stoichiometry, energy conservation, entropy production, and population positivity; (v) maximum-entropy equilibrium calculations yielding a unique thermal state; (vi) spectral relaxation analysis demonstrating the presence of near-zero modes rooted in disconnected momentum bins; and (vii) an adaptive momentum-grid extension that separates kinematic reachability from dynamical suppression.

The framework predicts, conditionally, an additional radiation density of ΔNeff≈0.043ΔNeff​≈0.043 and a relic abundance of Ωah2≈4.2×10−6Ωa​h2≈4.2×10−6 under a standard relativistic decoupling at g∗s=75g∗s​=75. The corresponding Higgs-sector predictions are a branching fraction of BR(H1→aa)≈4.81×10−4BR(H1​→aa)≈4.81×10−4 and a coupling modifier 1−κh2≈7.45×10−41−κh2​≈7.45×10−4. All predictions are consistent with current Planck and LHC constraints, though below the sensitivity of planned experiments. Falsification criteria are established. The framework is mathematically consistent, computationally validated, and experimentally untested — a status we deem appropriate for a first-principles program at this stage.

Keywords: TQTU, FQCU, Coherent Three-Scalar Framework, Higgs Portal, Boltzmann Solver, Thermal Decoupling, Maximum Entropy, Detailed Balance, Chemical Kinetics.
Part I — Theoretical Foundations
Chapter 1. Introduction: The Higgs–FQCU Program
1.1 The problem

The 2012 discovery of the 125 GeV Higgs boson completed the Standard Model as a renormalizable description of electroweak interactions up to the TeV scale. Subsequent programmatic work has focused on:

    Precision measurement of Higgs coupling modifiers κiκi​;

    Extensions with additional scalar multiplets (2HDM, singlet extensions, composite Higgs);

    Searches for WIMP-type and axion-like dark matter;

    Cosmological imprints of light relics through NeffNeff​.

The present work addresses a question at the intersection of (2) and (4): can a coherent multi-scalar extension of the Higgs sector be constructed such that (i) the low-energy scattering amplitude is algebraically suppressed, (ii) an ultra-light angular mode survives as a relic, and (iii) the resulting cosmological and collider signatures are simultaneously computable and mutually consistent?
1.2 The TQTU program

The TQTU research program proposes such a construction. Its essential ingredients are:

    A three-scalar coherent propagator with an exact partial-fraction cancellation;

    A light angular scalar of mass ma=4.135667696 meVma​=4.135667696 meV arising as a pseudo-Goldstone mode of a hidden U(1)U(1);

    A reduced, resonance-safe Boltzmann calculation for thermal decoupling, with explicit identification of which channels are and are not yet included.

1.3 Scientific methodology

This monograph is a review and synthesis, not a claim of discovery. Its central methodological commitments are:

    Every numerical result is traceable to a specific derivation or computation;

    Every open calculation is explicitly labeled as pending;

    No post-hoc parameter tuning is permitted after comparison with data;

    Falsification criteria are stated before any observational test;

    Negative results are published with the same rigor as positive results.

Chapter 2. The Coherent Three-Scalar Propagator
2.1 Mass matrix and benchmark parameters

The CP-even scalar sector consists of the SM-like Higgs hh, a hidden radial mode ϕϕ, and a heavy mediator xx. After symmetry breaking, the mass matrix in the (h,ϕ,x)(h,ϕ,x) basis reads:
Meven2=(2λHv2κ0vfαvκ0vf2λΨf2βfαvβfMX2)
Meven2​=
​2λH​v2κ0​vfαv​κ0​vf2λΨ​f2βf​αvβfMX2​​
​

with benchmark values:
Quantity	Value
m1m1​	125.09 GeV
m2m2​	500 GeV
m3m3​	1006.61 GeV
ff	1000 GeV
vv	246 GeV
α=βα=β	97.60147386 GeV
κ0κ0​	0

Vacuum displacement: The trilinear couplings αXH†HαXH†H and βX∣Ψ∣2βX∣Ψ∣2 imply a nonzero mediator VEV:
x0=−αv2+βf22MX2≈−51.1 GeV
x0​=−2MX2​αv2+βf2​≈−51.1 GeV

This must be included in the tadpole equations for the mass matrix to be an exact Hessian.
2.2 Partial-fraction decomposition and sum rule

The coherent propagator for ffˉ→aaffˉ​→aa mediated by the three mass eigenstates is:
P(s)=αβv s(s−m12)(s−m22)(s−m32)
P(s)=(s−m12​)(s−m22​)(s−m32​)αβvs​

Decomposing into simple poles:
P(s)=∑i=13Ris−mi2
P(s)=i=1∑3​s−mi2​Ri​​

one finds an exact algebraic identity:
∑i=13Rimi2=0
i=1∑3​mi2​Ri​​=0​

This is the Coherent Interference Sum Rule. It removes the constant low-energy contact term and leaves:
P(s)≃−CPs,CP≃5.912×10−10 GeV−3
P(s)≃−CP​s,CP​≃5.912×10−10 GeV−3
2.3 Low-energy suppression of the annihilation cross-section

The spin- and color-averaged cross section is:
σffˉ→aa(s)=mf264πNcv2 βfβa ∣P(s)∣2
σffˉ​→aa​(s)=64πNc​v2mf2​​βf​βa​∣P(s)∣2

At low ss:
∣P∣2≈CP2s2  ⟹  σffˉ→aa≈mf2CP264πNcv2 s2
∣P∣2≈CP2​s2⟹σffˉ​→aa​≈64πNc​v2mf2​CP2​​s2

Conventional single-mediator Higgs portals scale as σ∝mf2σ∝mf2​. The coherent three-mediator amplitude scales as σ∝mf2s2σ∝mf2​s2. This strongly suppresses the fermionic annihilation rate at late times.
Part II — Thermal Reaction Densities
Chapter 3. Fermionic Thermal Reaction Densities
3.1 Reaction-density integral

For a species ff in Maxwell–Boltzmann equilibrium:
γf(T)=gf2T32π4∫4mf2smax⁡ds (s−4mf2)s K1 ⁣(sT)σf(s)
γf​(T)=32π4gf2​T​∫4mf2​smax​​ds(s−4mf2​)s
​K1​(Ts
​​)σf​(s)

with gf=6gf​=6 (quarks) or 22 (charged leptons). The production diagnostic is:
Rf(T)=2γf(T)naeq(T) H(T)
Rf​(T)=naeq​(T)H(T)2γf​(T)​

with naeq=ζ(3)T3/π2naeq​=ζ(3)T3/π2 and H(T)=1.66g∗ T2/MPlH(T)=1.66g∗​
​T2/MPl​.

Linearization: In the near-equilibrium regime, Γchem(f)/H=RfΓchem(f)​/H=Rf​.
3.2 Reference numerical values

With g∗=75g∗​=75, zero-width propagator, smax⁡=900smax​=900 GeV22:
TT (GeV)	Bottom	Charm	Tau	Muon
0.5	2.23×10−82.23×10−8	1.24×10−61.24×10−6	3.74×10−73.74×10−7	6.59×10−96.59×10−9
1.0	1.14×10−41.14×10−4	7.55×10−57.55×10−5	4.03×10−54.03×10−5	2.14×10−72.14×10−7
2.0	1.82×10−21.82×10−2	2.83×10−32.83×10−3	1.76×10−31.76×10−3	6.88×10−66.88×10−6
3.0	1.38×10−11.38×10−1	1.69×10−21.69×10−2	1.08×10−21.08×10−2	4.02×10−54.02×10−5
4.0	3.56×10−13.56×10−1	4.09×10−24.09×10−2	2.61×10−22.61×10−2	9.65×10−59.65×10−5

The bottom channel dominates at T≳2T≳2 GeV due to its large Yukawa yb=mb/vyb​=mb​/v.
3.3 Extended-cutoff convergence

Extending smax⁡smax​ to s=110s
​=110 GeV increases the rate significantly:
TT (GeV)	30 GeV	60 GeV	80 GeV	110 GeV
2.0	0.0228	0.0238	0.0238	0.0238
3.0	0.1658	0.2506	0.2512	0.2512
4.0	0.4226	1.2174	1.2744	1.2804
5.0	0.6637	3.7311	4.4867	4.7244

The high-energy Boltzmann tail dominates at multi-GeV temperatures.
3.4 Higgs decay–inverse decay

The on-shell contribution is:
Γchem(D)(T)=2mH2ζ(3)T2K1(mH/T)ΓH→aa
Γchem(D)​(T)=ζ(3)T22mH2​​K1​(mH​/T)ΓH→aa​

with ΓH→aa=1.95756463×10−6ΓH→aa​=1.95756463×10−6 GeV. Under g∗=75g∗​=75:
TT (GeV)	Γchem(D)/HΓchem(D)​/H
2.0	2.96×10−132.96×10−13
3.0	8.15×10−58.15×10−5
4.0	1.0051.005
5.0	2.40×1022.40×102

Crossing: T×(D)≃3.999T×(D)​≃3.999 GeV.

Combined rate: Γtotal/H=Rfermions+Γchem(D)/HΓtotal​/H=Rfermions​+Γchem(D)​/H. At T=4T=4 GeV: 1.28+1.005=2.291.28+1.005=2.29.

Conclusion: The combined rate exceeds unity for T≳3.7T≳3.7 GeV. The physical decoupling is around 3.53.5–3.73.7 GeV, not 4.0 GeV.
Part III — Resonance-Safe Solver Architecture
Chapter 4. A Resonance-Safe Solver
4.1 Why a resonance-safe solver is necessary

Near a pole, the zero-width propagator diverges. Finite-width regularization:
Di(s)=1s−mi2+imiΓi
Di​(s)=s−mi2​+imi​Γi​1​

is required. But finite widths alone do not eliminate double-counting. If the Higgs is treated as an explicit thermal species, the process ffˉ→H1→aaffˉ​→H1​→aa overlaps with real Higgs production followed by H1→aaH1​→aa.
4.2 Two consistent strategies

    Strategy A (Explicit mediator): Evolve the angular scalar together with explicit Higgs-like species. Include nonresonant scattering without counting on-shell production twice.

    Strategy B (Effective collision kernel): Integrate out mediators where the EFT approximation is valid.

Recommended for FQCU benchmark: Strategy A near the electroweak scale; Strategy B below the lightest scalar mass. A matching procedure is needed between regimes.
4.3 The full phase-space Boltzmann equation
(∂∂t−Hp∂∂p)fa(p,t)=Catotal[f]
(∂t∂​−Hp∂p∂​)fa​(p,t)=Catotal​[f]

with
Catotal=Cdecay+Cinverse+Cnonresonant+Celastic+Cadditional
Catotal​=Cdecay​+Cinverse​+Cnonresonant​+Celastic​+Cadditional​
4.4 Detailed balance as a mandatory test

For 1+2↔3+41+2↔3+4, the quantum-statistical gain-minus-loss factor is:
F=f1f2(1±f3)(1±f4)−f3f4(1±f1)(1±f2)
F=f1​f2​(1±f3​)(1±f4​)−f3​f4​(1±f1​)(1±f2​)

At equilibrium, Feq=0Feq​=0 must hold numerically for every reaction.
4.5 Chemical relaxation rate

For small deviations, the linearized collision equation becomes:
δn˙a+3Hδna≃−Kμ(T)μa
δn˙a​+3Hδna​≃−Kμ​(T)μa​

with chemical-relaxation rate:
Γchem(T)=Kμ(T)χa(T)
Γchem​(T)=χa​(T)Kμ​(T)​

where χa=T2/6χa​=T2/6 for a massless boson.
4.6 Chemical potential susceptibility

For a bosonic species, define z(E)=f(E)/(1+f(E))z(E)=f(E)/(1+f(E)). In equilibrium, ln⁡z=−(E−μ)/Tlnz=−(E−μ)/T, linear in EE. This observation will be central to the log-fugacity correction of Chapter 8.
Part IV — Reduced Boltzmann Solver
Chapter 5. A Reproducible Boltzmann Solver
5.1 The reduced equation

For a single species in a radiation-dominated background:
dYadN=2γtotaleqsH[1−(YaYaeq)2]
dNdYa​​=sH2γtotaleq​​[1−(Yaeq​Ya​​)2]

with N=ln⁡aFRWN=lnaFRW​.
5.2 Analytical benchmark

Before physical applications, the solver is verified against the analytically solvable ODE:
dydN=r(N)(1−y2),r(N)=r0e−pN
dNdy​=r(N)(1−y2),r(N)=r0​e−pN

with exact solution involving arctan⁡arctan. The verified error tolerance:
ϵmax⁡=1.19×10−10
ϵmax​=1.19×10−10
5.3 Reduced freeze-out calculation

With frozen Higgs parameters (g∗=75g∗​=75), the reduced crossing is:
T×(D)=3.9992712 GeV
T×(D)​=3.9992712 GeV

The numerical abundance reaches y→1y→1 (equilibrium) before the decay-rate crossing. But this is a reduced-equation result; it does not by itself establish a physical decoupling.
5.4 Numerical/scientific audit
Test	Result
Analytical ODE benchmark	Passed, error 1.19×10−101.19×10−10
Frozen Higgs decay width	Preserved
Decay-rate crossing	3.9992712 GeV
Reduced thermalization trajectory	Computed
Exact Bose–Einstein collision kernel	Not implemented
Three-scalar scattering network	Not implemented
Realistic Standard Model EOS	Not implemented
Physical chemical decoupling	Not established
Part V — Quantum Kinetics
Chapter 6. Quantum-Statistical Collision Operator
6.1 The decay–inverse-decay operator
Ca(p1)=12E1∫dΠH dΠ2 (2π)4δ(4)(pH−p1−p2)∣MHaa∣2 F
Ca​(p1​)=2E1​1​∫dΠH​dΠ2​(2π)4δ(4)(pH​−p1​−p2​)∣MHaa​∣2F

with
F=fH(1+f1)(1+f2)−(1+fH)f1f2
F=fH​(1+f1​)(1+f2​)−(1+fH​)f1​f2​
6.2 Exact detailed balance

At equilibrium with fieq=1/(e(Ei−μi)/T−1)fieq​=1/(e(Ei​−μi​)/T−1):
1+fi=e(Ei−μi)/Tfi
1+fi​=e(Ei​−μi​)/Tfi​

Substituting yields:
F=fHf1f2[e(E1+E2−μ1−μ2)/T−e(EH−μH)/T]
F=fH​f1​f2​[e(E1​+E2​−μ1​−μ2​)/T−e(EH​−μH​)/T]

Energy conservation EH=E1+E2EH​=E1​+E2​ and chemical equilibrium μH=2μaμH​=2μa​ give Feq=0Feq​=0.
6.3 Chemical susceptibility

For massless boson:
χa=T26
χa​=6T2​

verified numerically to machine precision.
Chapter 7. Momentum-Resolved Collision Integration
7.1 Two-body kinematics

For a Higgs with momentum PP:
E1,2=EH±Pβ∗u2,β∗=1−4ma2/mH2
E1,2​=2EH​±Pβ∗​u​,β∗​=1−4ma2​/mH2​
​

with u∈[−1,1]u∈[−1,1] the rest-frame emission angle.
7.2 Collision kernel
Ca(p)=g216πp2∫p+mH2/(4p)∞dEH F
Ca​(p)=16πp2g2​∫p+mH2​/(4p)∞​dEH​F

Numerically:
pp	Ca(c=0.5)Ca​(c=0.5)	Ca(c=1.5)Ca​(c=1.5)
5 GeV	+1.419×10−38+1.419×10−38	−3.007×10−38−3.007×10−38
10 GeV	+1.655×10−22+1.655×10−22	−3.116×10−22−3.116×10−22
20 GeV	+4.187×10−15+4.187×10−15	−7.256×10−15−7.256×10−15

The extreme suppression reflects the Boltzmann tail of the Higgs distribution at T=10T=10 GeV. The integrated rate is dominated by p≈62.5p≈62.5 GeV.
7.3 Integrated number and energy transfer

At T=10T=10 GeV:
Quantity	c=0.5c=0.5	c=1.5c=1.5
dna/dtdna​/dt (GeV44)	+3.14×10−8+3.14×10−8	−5.24×10−8−5.24×10−8
dρa/dtdρa​/dt (GeV55)	+2.21×10−6+2.21×10−6	−3.67×10−6−3.67×10−6

Cross-section with §139 gives agreement to 0.16%0.16% (number) and 0.37%0.37% (energy).
Part VI — Multi-Momentum Evolution
Chapter 8. Conservative Collision Mapping and the Log-Fugacity Correction
8.1 Conservative mapping

For daughter energy EE between grid points Ej,Ej+1Ej​,Ej+1​:
wj=Ej+1−EEj+1−Ej,wj+1=E−EjEj+1−Ej
wj​=Ej+1​−Ej​Ej+1​−E​,wj+1​=Ej+1​−Ej​E−Ej​​

This preserves number (wj+wj+1=1wj​+wj+1​=1) and energy (wjEj+wj+1Ej+1=Ewj​Ej​+wj+1​Ej+1​=E).
8.2 The equilibrium drift problem

Linear interpolation of ff does not preserve the Bose–Einstein form between nodes. This produces an artificial collision flux even in thermal equilibrium.
8.3 Log-fugacity interpolation

Define:
L(E)=ln⁡(f(E)1+f(E))
L(E)=ln(1+f(E)f(E)​)

For BE, L(E)=−(E−μ)/TL(E)=−(E−μ)/T is linear in EE. Interpolating LL and reconstructing f=eL/(1−eL)f=eL/(1−eL) is exact for BE.

Result:
Grid	Linear interp (GeV44)	Corrected (GeV44)
12×60×812×60×8	−6.30×10−9−6.30×10−9	−9.96×10−24−9.96×10−24
18×90×1618×90×16	−2.59×10−9−2.59×10−9	−2.28×10−23−2.28×10−23
24×120×2424×120×24	−1.35×10−9−1.35×10−9	+5.83×10−24+5.83×10−24

14 orders of magnitude reduction.
8.4 Stationary equilibrium test

With both species initialized at BE equilibrium:
Test	Original	Corrected
Max relative Higgs change	1.24%	1.14×10−161.14×10−16
Energy drift	4.55×10−134.55×10−13	∼0∼0
Stoichiometric drift	−1.42×10−14−1.42×10−14	∼0∼0

Key insight: Energy conservation ⇏⇒ detailed balance. The correction is mathematically grounded in the multiplicative structure zH=z1z2zH​=z1​z2​ of BE detailed balance.
8.5 Convergence
Grid	Initial dna/dtdna​/dt (GeV44)
12×60×812×60×8	3.2101×10−83.2101×10−8
18×90×1618×90×16	3.1726×10−83.1726×10−8
24×120×2424×120×24	3.1594×10−83.1594×10−8

Relative difference between finest grids: 0.42%0.42%. Independent dimension refinement still pending.
Part VII — Entropy and Spectral Analysis
Chapter 9. Maximum-Entropy Equilibrium
9.1 Conserved quantities

For the isolated system: Q=na+2nHQ=na​+2nH​, ρtotal=ρa+ρHρtotal​=ρa​+ρH​.
9.2 Concavity
σ(f)=(1+f)ln⁡(1+f)−fln⁡f,σ′′(f)=−1f(1+f)<0
σ(f)=(1+f)ln(1+f)−flnf,σ′′(f)=−f(1+f)1​<0

Strict concavity guarantees a unique maximum.
9.3 Numerical equilibrium

Reference grid 12×60×812×60×8:
Teq=9.483007 GeV,μa=−4.232156 GeV
Teq​=9.483007 GeV,μa​=−4.232156 GeV

with μH=−8.464313μH​=−8.464313 GeV. Conservation residuals: ΔQ/Q0=−2.32×10−16ΔQ/Q0​=−2.32×10−16, Δρ/ρ0=1.37×10−16Δρ/ρ0​=1.37×10−16. Collision residual: 2.55×10−242.55×10−24.
9.4 The thermalization gap
S0=259.863361 GeV3,Smax⁡=260.163907 GeV3
S0​=259.863361 GeV3,Smax​=260.163907 GeV3

After t=10,000t=10,000 GeV−1−1: fraction of gap closed =0.07285%=0.07285%​.
Chapter 10. Spectral Relaxation
10.1 Linearized operator
dδydt=Jδy,Jij=∂Ci∂yj∣yeq
dtdδy​=Jδy,Jij​=∂yj​∂Ci​​
​yeq​​

The Jacobian is similar to a symmetric positive-semidefinite matrix; no exponentially growing instabilities.
10.2 Hidden near-zero modes

Beyond the 2 physical conservation laws, the finite-grid decay operator exhibits:

    Coarse grid (12×60×812×60×8): 41 near-zero modes

    Fine grid (18×90×1618×90×16): 60 near-zero modes

Some momentum bins are weakly coupled or disconnected by pure decay-inverse-decay kinematics.
10.3 Timescales
γfast≈1.956×10−6 GeV  ⟹  τfast≈5.11×105 GeV−1
γfast​≈1.956×10−6 GeV⟹τfast​≈5.11×105 GeV−1
γslow∼10−15 GeV  ⟹  τslow∼1015 GeV−1
γslow​∼10−15 GeV⟹τslow​∼1015 GeV−1

The simulation interval 104104 GeV−1−1 is shorter than τfastτfast​, explaining the slow entropy gap closure.
Chapter 11. Collision-Network Rank
11.1 The reaction-event matrix
dNdt=VR
dtdN​=VR

Each column of VV represents net population changes from one event. Nullity =Nvar−rank(V)=Nvar​−rank(V).
11.2 Numerical rank
Grid	NvarNvar​	rank(V)rank(V)	Nullity
12×60×812×60×8	72	31	41
18×90×1618×90×16	108	49	59
24×120×2424×120×24	144	67	77
11.3 Nullity decomposition
Nullity=Nuntouched+2
Nullity=Nuntouched​+2

The +2+2 accounts for the conservation laws (QQ and ρρ). Extra zero modes are explained by kinematic reachability truncation, not new physics.
11.4 Structural vs. dynamical rank

    Structural rank of VV: which population combinations can change in principle

    Relaxation spectrum of JJ: how rapidly connected modes approach equilibrium

Thermal Boltzmann suppression (e−E/Te−E/T) can render connected modes sluggish (τ∼1015τ∼1015 GeV−1−1), explaining slow entropy closure.
Part VIII — Adaptive Grids and Unified Consistency
Chapter 12. Adaptive Momentum Extension
12.1 Cutoff convergence at T=10T=10 GeV
Pmax⁡Pmax​ (GeV)	Rate (GeV44)	Relative diff from 1200
100	2.905×10−82.905×10−8	7.573%
150	3.133×10−83.133×10−8	0.319%
220	3.143×10−83.143×10−8	0.0014%
400	3.142582×10−83.142582×10−8	1.5×10−121.5×10−12

Reference: dna/dt=3.142582221566×10−8dna​/dt=3.142582221566×10−8 GeV44.
12.2 Temperature-dependent cutoff

At higher TT, the required Pmax⁡Pmax​ increases. A fixed 220 GeV cutoff misses 45% of the integrated rate at T=100T=100 GeV.

Adaptive cutoff rule:
Pmax⁡(T)=min⁡{P:ϵ(P,T)<ϵtol}
Pmax​(T)=min{P:ϵ(P,T)<ϵtol​}

with ϵtol=10−4ϵtol​=10−4.
Temperature	First scanning cutoff below 0.01%
5 GeV	129.7 GeV
10 GeV	197.9 GeV
25 GeV	379.3 GeV
50 GeV	681.0 GeV
100 GeV	1214.0 GeV
12.3 The key distinction
Integrated rate convergence≠spectral convergence
Integrated rate convergence=spectral convergence​
Chapter 13. Unified Consistency Tests
13.1 Mass-consistent phase-space

For a massive boson:
dn=EE2−m22π2f(E) dE
dn=2π2EE2−m2
​​f(E)dE

This replaces the massless E2dE/(2π2)E2dE/(2π2) — negligible for FQCU but essential for general solvers.
13.2 Five mandatory tests
Test	Result
Stoichiometric conservation	ΔQ/Q≤10−14ΔQ/Q≤10−14
Energy conservation	Δρ/ρ≤10−16Δρ/ρ≤10−16
Bose–Einstein detailed balance	Residual ∼10−24∼10−24 GeV44
Entropy production	dS/dt>0dS/dt>0 throughout
Population positivity	fmin⁡>0fmin​>0
13.3 The convergence discrepancy

Initial scalar-production rate:

    Grid A (12×60×812×60×8): 3.2100989×10−83.2100989×10−8 GeV44

    Grid B (18×90×1618×90×16): 3.1725669×10−83.1725669×10−8 GeV44

Relative difference: 1.18%1.18%.
13.4 Error budget framework
ϵtotal=ϵmomentum+ϵenergy+ϵangular+ϵcutoff
ϵtotal​=ϵmomentum​+ϵenergy​+ϵangular​+ϵcutoff​

Each contribution must be isolated by independent grid refinement before a fully cosmological solver can be claimed.
Part IX — Predictions and Falsification
Chapter 14. Conditional Predictions
14.1 Cosmological

Under g∗s(Tdec)=75g∗s​(Tdec​)=75:
ΔNeff≈0.043,Ωah2≈4.2×10−6
ΔNeff​≈0.043,Ωa​h2≈4.2×10−6

Under the self-consistent value g∗s(Tdec)≈65g∗s​(Tdec​)≈65 at Tdec≈3.7Tdec​≈3.7 GeV:
ΔNeff≈0.063,Ωah2≈6.2×10−6
ΔNeff​≈0.063,Ωa​h2≈6.2×10−6

Both scenarios are presented as conditional.
14.2 Collider
BR(H1→aa)≈4.81×10−4
BR(H1​→aa)≈4.81×10−4
1−κh2≈7.45×10−4
1−κh2​≈7.45×10−4
μHiggs≈0.9988
μHiggs​≈0.9988
14.3 Comparison with current data
Observable	Prediction	Current sensitivity	Status
ΔNeffΔNeff​	0.043–0.063	Planck ±0.17±0.17	Invisible
ΔNeffΔNeff​	0.043–0.063	CMB-S4 ±0.03±0.03	Marginal
BRinvBRinv​	4.81×10−44.81×10−4	LHC ≲0.1≲0.1	Invisible
1−κh21−κh2​	7.45×10−47.45×10−4	HL-LHC ≲0.02≲0.02	Invisible
Matter power	∼10−5∼10−5	Any survey	Unobservable

The framework is consistent with all current data but below the sensitivity of planned experiments.
Chapter 15. Falsification Criteria

Pre-registered:

    A measurement of ΔNeff<0.01ΔNeff​<0.01 at 3σ3σ rules out all three scenarios.

    A measurement of ΔNeff>0.1ΔNeff​>0.1 at 3σ3σ rules out the intermediate scenario.

    A measurement of BRinv<10−4BRinv​<10−4 at 3σ3σ rules out the tree-level H1→aaH1​→aa decay.

    A measurement of 1−κh21−κh2​ inconsistent with 7.45×10−47.45×10−4 at 3σ3σ rules out the benchmark mixing.

    Evidence for self-interacting dark radiation invalidates the free-streaming assumption.

Part X — Open Problems and Future Directions
Chapter 16. What Remains Unresolved
16.1 Thermal history

The full collision-network evolution including all channels (ffˉ→aaffˉ​→aa, VV→aaVV→aa, gg→aagg→aa, heavy-scalar decays, elastic af→afaf→af) has not been computed. The current ΔNeffΔNeff​ remains conditional.
16.2 Coherent propagator derivation

The sum rule ∑Ri/mi2=0∑Ri​/mi2​=0 is verified algebraically for the rational function. A full microscopic derivation from the frozen Lagrangian — including resummation of off-diagonal self-energies — remains an outstanding requirement.
16.3 Reheating temperature

The relic abundance depends on whether the post-inflationary plasma reached temperatures where Higgs-mediated production was efficient. Three benchmark reheating scenarios should be tabulated.
16.4 Cosmological expansion

The current solver assumes a non-expanding background. The Hp∂pfHp∂p​f term must be added for the physical freeze-out calculation.
16.5 Spectral equilibration

Elastic scattering (af→afaf→af) is required for kinetic equilibrium. Without it, high-energy modes accumulate energy that cannot cascade to low-EE.
16.6 Independent grid convergence

Individual ϵmomentumϵmomentum​, ϵenergyϵenergy​, ϵangularϵangular​, ϵcutoffϵcutoff​ remain to be isolated.
Chapter 17. Roadmap

The natural progression:

    Derive the coherent propagator from the frozen Lagrangian (Q1).

    Compute the full chemical-relaxation eigenvalue including all channels (Q1–Q2).

    Implement the momentum-dependent coupled Boltzmann solver with quantum statistics (Q2).

    Determine TdecTdec​ and g∗s(Tdec)g∗s​(Tdec​) self-consistently (Q2).

    Recompute CMB CℓCℓ​ with a validated perturbation solver (Q3).

    Register all predictions in a public registry with provenance labels (Q3).

Part XI — Conclusion
Chapter 18. Final Scientific Statement

The Higgs–FQCU Coherent Three-Scalar Framework is a self-consistent, falsifiable extension of the Standard Model that combines:

    An algebraic low-energy suppression mechanism (∑Ri/mi2=0∑Ri​/mi2​=0);

    A computable thermal history with a resonance-safe Boltzmann solver;

    Explicit laboratory predictions (BRinvBRinv​, κhκh​, μHiggsμHiggs​);

    Numerical validation via five mandatory consistency tests.

Its predictions are not in conflict with any current data. They are, however, below the sensitivity of any currently planned experiment, and several derivations required to promote them from conditional to derived have not yet been completed.

The framework is mathematically consistent, computationally validated, and experimentally untested.

This status is appropriate for a first-principles program at this stage. The next decade of experimental cosmology and collider physics will determine whether the FQCU prediction can be distinguished from the Standard Model or whether the framework must be re-examined.
Appendices
Appendix A. Numerical Code Listings

The following scripts are available in the TVRI public repository:

    higgs_fqcu_section133.py — Thermal reaction densities

    higgs_fqcu_section138.py — Quantum collision test

    higgs_fqcu_section139.py — Momentum-resolved collision

    higgs_fqcu_section140.py — Coupled conservation solver

    higgs_fqcu_section141.py — Coupled kinetic solver

    higgs_fqcu_section142.py — Multi-momentum coupled solver

    higgs_fqcu_section143.py — Detailed balance correction

    higgs_fqcu_section145.py — Maximum-entropy equilibrium

    higgs_fqcu_section146.py — Spectral relaxation analysis

    higgs_fqcu_section147.py — Collision rank computation

    higgs_fqcu_section148.py — Cutoff convergence

    higgs_fqcu_section149.py — Phase-space weights

    higgs_fqcu_section150.py — Unified consistency tests

All scripts depend only on NumPy and SciPy.
Appendix B. Frozen Benchmark Registry
Quantity	Value	Provenance
mama​	4.135667696 meV	Frozen input
m1m1​	125.09 GeV	Frozen input (calibrated to LHC)
m2m2​	500 GeV	Frozen input
m3m3​	1006.61 GeV	Frozen input
vv	246 GeV	Standard electroweak
ff	1000 GeV	Frozen input
α=βα=β	97.60147386 GeV	Frozen input
κ0κ0​	0	Benchmark choice
ΓH→aaΓH→aa​	1.95756463×10−61.95756463×10−6 GeV	Derived (tree-level)
Appendix C. Status of Predictions
Quantity	Value	Status
∑Ri/mi2=0∑Ri​/mi2​=0	Exact	Algebraic consequence
CPCP​	5.912×10−105.912×10−10 GeV−3−3	Derived
Rfermions(4 GeV)Rfermions​(4 GeV)	0.42–1.28	Truncated-integral range
Γchem(D)/H(4 GeV)Γchem(D)​/H(4 GeV)	1.005	Reduced-model numerical
TdecTdec​	∼3.7∼3.7 GeV	Combined crossing
ΔNeffΔNeff​	0.043–0.063	Conditional
Ωah2Ωa​h2	4.2–6.2×10−64.2–6.2×10−6	Conditional
BR(H1→aa)BR(H1​→aa)	4.81×10−44.81×10−4	Tree-level
1−κh21−κh2​	7.45×10−47.45×10−4	Tree-level
Full chemical-relaxation eigenvalue	Pending	
Physical decoupling temperature	Not established	
Unique ΔNeffΔNeff​ prediction	Not established	
Appendix D. Full Bibliography

[1] Chowdhury, M. F. I. (2026). The TQTU-FQCU Framework: A Consolidated Manuscript v6.0. TVRI Preprint.

[2] Hu, W., Eisenstein, D. J., & Tegmark, M. (1998). Cosmological perturbations and massive neutrino structures. Astrophysical Journal, 502, 1.

[3] Zubarev, D. N. (1974). Nonequilibrium Statistical Thermodynamics. Consultants Bureau.

[4] Lelli, F., McGaugh, S. S., & Schombert, J. M. (2016). SPARC: Mass models for 175 disk galaxies. The Astronomical Journal, 152(6), 157.

[5] Planck Collaboration (2020). Planck 2018 results. VI. Cosmological parameters. Astronomy & Astrophysics, 641, A6.

[6] Particle Data Group (2024). Review of Particle Physics. Physical Review D, 110, 030001.

[7] Chowdhury, M. F. I. (2026). TQTU-FQCU Master Field Equation v7.6. TVRI Preprint.

[8] Hannestad, S., & Madsen, J. (1995). Neutrino decoupling in the early universe. Physical Review D, 52, 1764.

[9] Kolb, E. W., & Turner, M. S. (1990). The Early Universe. Addison-Wesley.

[10] Dodelson, S. (2003). Modern Cosmology. Academic Press.

[11] Ma, C.-P., & Bertschinger, E. (1995). Cosmological perturbation theory in the synchronous and conformal Newtonian gauges. Astrophysical Journal, 455, 7.

[12] Arnold, P., & Espinosa, O. (1993). Effective potential and first-order phase transitions. Physical Review D, 47, 3546.

[13] Dolan, L., & Jackiw, R. (1974). Symmetry behavior at finite temperature. Physical Review D, 9, 3320.

[14] Tegmark, M., Zaldarriaga, M., & Seljak, U. (1997). Microwave background constraints on cosmological parameters. Astrophysical Journal, 480, 22.

[15] Hairer, E., & Wanner, G. (1996). Solving Ordinary Differential Equations II. Springer.

All discoveries herein are by the mercy of Allah. This knowledge is a trust.

Monograph Summary
Section	Chapters	Source Articles
Part I: Foundations	1–2	A1
Part II: Thermal Rates	3	A2
Part III: Solver Architecture	4	A3
Part IV: Reduced Solver	5	B2
Part V: Quantum Kinetics	6–7	B1
Part VI: Multi-Momentum	8	B3
Part VII: Entropy & Spectral	9–11	C1, C2
Part VIII: Adaptive Grids & Consistency	12–13	D1, D2
Part IX: Predictions	14–15	Cross-cutting
Part X: Open Problems	16–17	Cross-cutting
Part XI: Conclusion	18	Cross-cutting

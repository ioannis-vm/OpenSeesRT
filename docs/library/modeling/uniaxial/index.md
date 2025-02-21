# UniaxialMaterial Library

The `opensees.uniaxial` module (or `uniaxialMaterial` Tcl command)
provide access to the library of models implementing the [`UniaxialMaterial`](/OpenSeesRT/developer/architecture/class_interface/material/UniaxialMaterial/)
interface. This interface represents a scalar-valued work-conjugate relationship
(e.g., uniaxial stress-strain, force-deformation, etc.) that is generally
path-dependent.

The valid queries to any uniaxial material when creating an
[`ElementRecorder`] are `strain`, `stress`, and `tangent`. Some materials
have additional queries to which they will respond. These are documented
in the NOTES section for those materials.


### General-Purpose Materials

#### Elastic / Path-Independent
<ul>
<li><a href="Elastic_Uniaxial_Material">Elastic</a></li>
<li><a href="Elastic-No_Tension_Material">Elastic-No Tension</a></li>
<li><a href="ElasticBilin_Material">ElasticBilin</a></li>
<li><a href="ElasticMultiLinear_Material">ElasticMultiLinear</a></li>
<li><a href="PathIndependent_Material">PathIndependent</a></li>
</ul>

#### Inelastic
<ul>
<li><a href="MultiLinear_Material">MultiLinear</a></li>
<li><a href="Elastic-Perfectly_Plastic_Gap">Elastic-Perfectly Plastic Gap</a></li>
<li><a href="Pinching4_Material">Pinching4</a></li>
</ul>

#### Standard Rate-Independent Materials
These models are formulated and implemented according to well-established
principles and algorithms.
<ul>
<li><a href="ElasticPP">ElasticPP</a> Elastic-perfectly plastic</li>
<li><a href="Hardening_Material">Hardening</a></li>
</ul>

#### Standard Rate-Dependent Materials
<ul>
<li><a href="Viscous_Material">Viscous</a></li>
<li><a href="ViscousDamper_Material">ViscousDamper</a></li>
</ul>


### Metallic 

<ul>
<li><a href="Hysteretic_Material">Hysteretic</a></li> 
<li><a href="RambergOsgoodSteel">RambergOsgoodSteel</a> A simple metalic model exhibiting a nonlinear hardening curve.</li>
<li><a href="Steel01">Steel01</a></li>
<li><a href="Steel02">Steel02</a> Giuffré-Menegotto-Pinto Model with Isotropic Strain Hardening</li>
<li><a href="SteelMPF">SteelMPF</a>
   Menegotto and Pinto (1973) model Extended by Filippou et al. (1983)</li>
<li><a href="Steel4">Steel4</a></li>   
<li><a href="DoddRestrepo">Dodd Restrepo</a> A new model which allows the "softness" of the Bauschinger curve, as determined by the area under the curve
  relative to the enclosing parallelogram, to be controlled.</li> 
<li><a href="Reinforcing_Steel_Material">ReinforcingSteel</a></li> 
<li><a href="UVCuniaxial_(Updated_Voce-Chaboche)">UVCuniaxial</a> Updated Voce-Chaboche</li>
</ul>


### Concrete

<ul>
<li><a href="Concrete01">Concrete01</a> Hognestad's concrete curve with zero tensile strength</li>
<li><a href="Concrete02">Concrete02</a> Concrete01 with linear tension softening</li>
<li><a href="Concrete04">Concrete04</a> Popovics concrete curve</li>
<li><a href="Concrete06">Concrete06</a> Thorenfeldt curve</li>
<li><a href="Concrete07">Concrete07</a> Chang &amp; Mander’s 1994 Concrete Model</li>
<li><a href="ConfinedConcrete01">ConfinedConcrete01</a></li>  
<li><a href="ConcreteD">ConcreteD</a>   concrete material based on the Chinese design code</li>
<li><a href="ConcreteCM">ConcreteCM</a> Complete Concrete Model by Chang and Mander (1994)</li>
<li><a href="FRPConfinedConcrete">FRPConfinedConcrete</a></li>
</ul>

### Bouc-Wen Models

<ul>
<li>BoucWenOriginal</li>
<li>DegradingPinchedBW</li>
<li>BoucWenInfill</li>
<li><a href="BoucWen_Material">BoucWen</a></li>
<li><a href="BWBN_Material">BWBN</a> Pinching Hysteretic Bouc-Wen Material</li>
</ul>
### Pinch and Slip

<ul>
<li><a href="SAWS_Material">SAWS</a> Pinching material for woodframed structures.</li>
</ul>

### Wrappers

<ul>
<li><a href="Parallel_Material">Parallel</a></li>
<li><a href="Series_Material">Series</a></li>
<li><a href="Initial_Strain_Material">Initial Strain</a></li>
<li><a href="Initial_Stress_Material">Initial Stress</a></li>
<li><a href="Fatigue_Material">Fatigue</a></li>
<li><a href="MinMax_Material">MinMax</a></li>
<li><em>SimpleFractureMaterial</em></li>
<li><em>ContinuumUniaxial</em> performs static condensation to impose a uniaxial state of stress on a three-dimensional `NDMaterial`</li>
</ul>

### Other Uniaxial Materials

<ul>
<li><a href="Concrete01WithSITC">Concrete01WithSITC</a>
Concrete Material With Stuff in the Cracks</li>

<li><a href="ModIMKBilin/">ModIMKBilin</a>
Modified Ibarra-Medina-Krawinkler Deterioration Model with Bilinear Hysteretic Response (Bilin)
</li>

<li><a href="ModIMKPeakOriented/">ModIMKPeakOriented</a>
Modified Ibarra-Medina-Krawinkler Deterioration Model with Peak-Oriented Hysteretic Response
</li>

<li><a href="ModIMKPinching">ModIMKPinching</a>
Modified Ibarra-Medina-Krawinkler Deterioration Model with Pinched Hysteretic Response
</li>

<li><a href="CastFuse">CastFuse</a></li>
<li><a href="BilinearOilDamper">BilinearOilDamper</a></li>
<li><a href="BARSLIP_Material">BARSLIP</a></li>
<li><a href="Bond_SP01">Bond_SP01</a>
Strain Penetration Model for Fully Anchored Steel Reinforcing Bars
</li>

<li><a href="Impact_Material">Impact</a></li>
<li><a href="Hyperbolic_Gap_Material">HyperbolicGap</a></li>

<li><a href="Engineered_Cementitious_Composites_Material">Engineered Cementitious Composites</a></li>


<li><a href="KikuchiAikenHDR_Material">KikuchiAikenHDR</a></li>
<li><a href="KikuchiAikenLRB_Material">KikuchiAikenLRB</a></li>
<li><a href="AxialSp_Material">AxialSp</a></li>
<li><a href="AxialSpHD_Material">AxialSpHD</a></li>

<li><a href="CFSWSWP">CFSWSWP</a> Wood-Sheathed Cold-Formed Steel Shear Wall Panel </li>
<li><a href="CFSSSWP">CFSSSWP</a> Steel-Sheathed Cold-formed Steel Shear Wall Panel</li>

<li><a href="SelfCentering_Material">SelfCentering</a> uniaxial self-centering (flag-shaped) material object with optional non-recoverable slip behaviour and an optional stiffness increase at high strains (bearing behaviour).</li>
</ul>

### PyTzQz uniaxial soil materials 

for p-y, t-z and q-z elements for modeling soil-structure interaction through the piles in a structural foundation
<ul>
  <li><a href="PySimple1">PySimple1</a></li>
  <li><a href="TzSimple1">TzSimple1</a></li>
  <li><a href="QzSimple1">QzSimple1</a></li>
  <li><a href="PyLiq1">PyLiq1</a></li>
  <li><a href="TzLiq1">TzLiq1</a></li>
  <li><a
    href="http://opensees.berkeley.edu/OpenSees/manuals/usermanual/1257.htm">PySimple1Gen Command</a></li>
  <li><a
    href="http://opensees.berkeley.edu/OpenSees/manuals/usermanual/1261.htm">TzSimple1Gen Command</a></li>
</ul>


### Frameworks
<ul>
<li><a href="Limit_State">Limit State</a></li>
<li>AlgebraicHysteresis</li>
</ul>


[`ElementRecorder`]: "/OpenSeesRT/library/4_Utilities/recorders/"


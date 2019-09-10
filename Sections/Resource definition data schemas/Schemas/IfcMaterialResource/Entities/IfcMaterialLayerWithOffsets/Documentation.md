﻿_IfcMaterialLayerWithOffsets_ is a specialization of _IfcMaterialLayer_ enabling definition of offset values along edges (within the material layer set usage in parent layer set).

It defines the assignment of two offset values for a material layer in its intended use within a material layer set. Offsets are applied to the edges of layered elements (that is, in directions perpendicular to the layer set direction). Offsets shall not be used in layer set direction, that is, for modelling gaps (or overlaps) between layers; gaps shall be modeled as layers with appropriate material assignment for the void.

> EXAMPLE &nbsp; At the top of a standard wall, with shape representation SweptSolid, offset of a given layer can be specified in the direction of the extrusion (positive Z axis), applied at the start or end (extruded from bottom to top), and with a positive (extending above extrusion) or negative (ending below extrusion).  
>   
> Take a standard wall with the outer material layer for the external isolation extending above extrusion by 100mm, but starting at the same base height. In this case the following values are set: <ul>
<li><small><em>OffsetDirection</em> = .AXIS3.</small></li>
<li><small><em>OffsetValues[1]</em> = 0.0</small></li>
<li><small><em>OffsetValues[2]</em> = 100.0 (default unit assumed to
be mm)</small></li></ul>

> HISTORY&nbsp; New entity in IFC4.

{ .spec-head}
Informal Propositions:

1. The _OffsetDirection_ shall not be identical to the _LayerSetDirection_ of the corresponding _IfcMaterialLayerSetUsage_.
2. The attribute ReferenceExtent shall be asserted at the corresponding _IfcMaterialLayerSetUsage_.

{ .use-head}
Attribute use definition

The _OffsetValues_ and _OffsetDirection_ correspond to the definitions _ReferenceExtent_ and _LayerSetDirection_ at the _IfcMaterialLayerSetUsage_. Figure 1 shows an example of applying the _OffsetValues_ to the material layers of a standard wall.

!["IfcMaterialLayerWithOffsets_fig-1"](../../../../../../figures/ifcmateriallayerwithoffsets_fig-1.png "Figure 1 &mdash; Material layer with offsets")
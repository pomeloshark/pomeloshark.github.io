---
layout: page
title: planetology
permalink: /worldbuilding/planetology.html
---

0. [Planet formation in depth](/worldbuilding/planetology/formation.html)
1. [Geosphere](/worldbuilding/planetology/geosphere.html)
2. [Hydrosphere](/worldbuilding/planetology/hydrosphere.html)
3. [Atmosphere](/worldbuilding/planetology/atmosphere.html)
4. [Climatology](/worldbuilding/planetology/climatology.html)
5. [Building](/worldbuilding/planetology/building.html)
6. [Mapping](/worldbuilding/planetology/mapping.html)

how things (probably) went on earth
- period of chaos in emerging solar system
  - the moon
- cooled earth and basalt
- oceans
- continents and beginnings of tectonic activity
- glaciation

## caps

mass
- 2.0 ± 0.7 (chen & kipping 2016)
- 2.0 (zeng et al 2016)

radius
- 1.48 +0.08 -0.04 (rogers 2015)
- 1.23 +0.44 -0.22 (chen & kipping 2016)
- 1.5 (lopez & fortney 2014)
- 1.2 (simpson 2016)

---

---

- surface formation
- internal structure and processes
- plate tectonics
- geologic provinces, mineral deposits & soils

---

- ocean circulation
- tides
- groundwater
- surface waters, fluvial processes

---

köppen classification scheme, trewartha modifications, holdridge life zones

## tropical climates

Af: tropical wet
: desc

Am: tropical monsoon

Aw & As: tropical savannah

## arid climates

BWh: subtropical or hot desert

BSh: subtropical or hot steppe

BWk: midlatitude or cold desert

BSk: midlatitude or cold steppe

## temperate climates

Csa: hot summer mediterranean

Csb: warm summer mediterranean

Csc: cold summer mediterranean

Cwa: humid subtropical

Cwb: subtropical highland

Cwc: temperate highland

Cfa: humid subtropical

Cfb: temperate oceanic

Cfc: subpolar oceanic

## continental climates

Dfa & Dsa: hot summer humid continental

Dfb & Dsb: warm summer humid continental

Dfc & Dsc: subarctic humid

Dfd & Dsd: extreme subarctic

Dwa: hot Manchurian

Dwb: warm Manchurian

Dwc: subarctic Manchurian

Dwd: extreme subarctic Manchurian

## polar climates

ET: tundra

EF: ice cap

## marine biomes

- seagrass meadows
- kelp forests
- coral reefs

## implement

-

## sources

---

implementing plate tectonics - some cheats for reverse engineering

The most realistic way to do this would be to start with some primordial cratons and build from there; [here](https://worldbuildingpasta.blogspot.com/2020/01/an-apple-pie-from-scratch-part-va.html) is a tutorial on how to do this using GPlates. However, I realize most of us (myself definitely included) have at least a vague notion of the map we want to work with, and so end up kind of working backwards and forwards simultaneously. It's not impossible, but it will keep you on your toes for a while.

Some points to keep in mind:
- Remember that the continents are not floating on top of the oceans: you need to account for the entire surface, not just the stuff that's above the water. It may be helpful to picture the ocean floor as the part that's moving, and any collisions of continents as by-products of that.
- Remember that you're working on the surface of a sphere. The movement of your continents is not constricted in any way by the edges of your map! Make heavy use of a tool like MapToGlobe so that you can better visualize this at all times.
- Don't panic if your existing landmasses don't line up well -- it's the edges of the continental shelves that need to line up, and sea levels are always changing.

geological resources - deposits and distribution

---

![Markdown Linter](https://github.com/Orange-OpenSource/ext_file_format/workflows/Markdown%20Linter/badge.svg)

# *Halles des Vosges*, Belfort, France

This sample is a demonstration of multi-material building with a slopped roof. At its base is a concrete wall, followed by glass towards the top. The main part has two slopes, divided in two parts each. Two smaller building are attached in the back, each with slopped roof too.

## Regions

![figure 1](./sectors.svg)  
*Figure 1 — Map of regions*

The building has been divided in 28 regions as seen in figure 1 each requiring an *.ext* file to describe the planes of the slopes.

Regions can share the same *.ext* file when sharing the same plane *i.e.* roof. Example : region 20 has its own plane hence its own *.ext*, region 1 shares its *.ext* with 2 other regions since the roofs share the same plane.

Some regions need to be subdivided. Example : region 2 and 3 share the same roof, but don't share inner materials. Region 2 is a concrete pillar while 3 is mainly glass with only a part of concrete.

## Before extrusion

![figure 2](./halles_GIS.png)  
*Figure 2 — Halles without .ext enhancement*

Without using *.ext* extrusion and basing the 3D model only on GIS vector data and height attributes, *les halles* resembles a cuboid in either glass or concrete and a flat roof, as seen in figure 2.

## Results

![figure 3](./halles_front.png) ![](./halles_back.png)  
*Figure 3 — Enhanced building front (left) and back (right)*

Figure 3 shows the result of the extrusion  of the building. Concrete is shown in grey, and glass in blue. The concrete wall only appears all around the building, hence the need to have the walls in separate regions. Inside, the 2m walls don't appear, ground level is respected.

Proportions are respected, this 3D model resembles faithfully reality.

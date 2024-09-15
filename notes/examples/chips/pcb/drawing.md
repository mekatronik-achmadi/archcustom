# KiCAD PCB Summary

## Drawing

### Create Plot Folder

create **plots** to store all plotted files

```sh
mkdir -p plots/
```

### Schematic

To generate schematic Landscape A4 PDF:

```
Schematic Editor: File -> Plot
```

![](images/sch_pdf.png)

In this example, resulted file renamed as **sch.pdf** in **plots** folder.

### PCB Layout

To generate layout PDF using Board2PDF extension:

```
PCB Editor: Tools -> External Plugins -> Board2Pdf
```

![](images/brd_pdf.png)

In this example, resulted file renamed as **brd.pdf** in **plots** folder.

### Wiring

First, generate PCB as **brd.svg** file in **plots** folder:

```
PCB Editor: File -> Export -> SVG
```

![](images/brd_svg.png)

Convert the **brd.svg** into DXF using Inkscape and PStoEdit:

```sh
inkscape -o brd.eps brd.svg
pstoedit -dt -f 'dxf:-polyaslines -mm' brd.eps brd.dxf
```

Then, use the result **brd.dxf** to draw wiring diagram using 2D CAD.

For example, import the DXF as block in LibreCAD:

```
LibreCAD: File -> Import -> Block
``` 

![](images/librecad.png)

Last, generate PDF from LibreCAD:

```
LibreCAD: File -> Export PDF -> Print
```

Choose **No** for fitting resize and rename the result to **wiring.pdf**.

![](images/cadpdf.png)

### Merge PDFs

Merge all PDFs into single file named **drawing.pdf**:

```sh
pdfjam --outfile drawing.pdf \
--paper a5paper --landscape \
wiring.pdf sch.pdf brd.pdf
```

## Fabrication

### View 3D

To get 3D View:

```
PCB Editor: View -> 3D Viewer
```

![](images/view3d.png)

### Gerbers

First create subfoler named **gerber**:

```sh
mkdir -p plots/gerber/
```

Then, generate Gerber files into that subfolder:

```
PCB Editor: File -> Fabrication Outputs -> Gerbers
```

![](images/grbr.png)

You can view Gerber result in KiCAD's Gerber Viewer

![](images/kigrbrview.png)

or using lighweight [GerbView](https://github.com/gerbv/gerbv)

![](images/gvgrbrview.png)

or using web-based [Tracespace](https://github.com/tracespace/tracespace).

![](images/tsgrbrview.png)

#### Board Size

Check board size from Gerber Job file

```sh
jq -M -r '.[].Size' plots/gerber/*.gbrjob 2> /dev/null
```

## Bill Of Material

Generate Bill of Material as CSV file into **plots** folder:

```
PCB Editor: File -> Fabrication Outputs -> BOM
```

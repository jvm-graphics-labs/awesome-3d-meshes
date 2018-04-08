# [The Stanford 3D Scanning Repository](http://graphics.stanford.edu/data/3Dscanrep/)

 In recent years, the number of range scanners and surface reconstruction algorithms has been growing 
 rapidly. Many researchers, however, do not have access to scanning facilities or dense polygonal 
 models. The purpose of this repository is to make some range data and detailed reconstructions 
 available to the public. Here's how the models in this repository were created:
 
##### Scanning and surface reconstruction

The first set of models below, called "The Stanford Models", were scanned with a [Cyberware](http://www.cyberware.com/) 
3030 MS scanner, with the exception of Lucy, who was scanned with the [Stanford Large Statue Scanner](http://graphics.stanford.edu/projects/mich/mgantry-in-lab/mgantry-in-lab.html),
 designed for the [Digital Michelangelo Project](http://graphics.stanford.edu/projects/mich/). 
 Both scanners are swept-stripe, laser triangulation range scanners. The triangulation calculations 
 all the Stanford models except the Happy Buddha and Dragon were performed in hardware by the 
 Cyberware scanner(s). These last two models were acquired using Brian Curless's [spacetime analysis](http://graphics.stanford.edu/papers/spacetime).
  Each scan takes the form of a range image, described in the local coordinate system of the scanner. 
  To merge these range images, we must first align them together. For all the Stanford models, 
  alignment was done using a modified ICP algorithm, as described in [this paper](http://graphics.stanford.edu/papers/zipper).
   These alignments are stored in ".conf" files, which list each range image in the model along with a 
   translation and a quaternion rotation. Finally, the aligned range images are combined to produce a
    single triangle mesh (a process sometimes called surface reconstruction) using either [zippering](http://graphics.stanford.edu/papers/zipper) 
    or [volumetric merging](http://graphics.stanford.edu/papers/volrange), two methods developed at 
    Stanford. The entry for each model indicates which method was used. Implementations of both 
    methods are currently available for download, respectively, at [ZipPack](http://graphics.stanford.edu/software/zippack/) 
    and [VripPack](http://graphics.stanford.edu/software/vrip/). The second method is the surface 
    reconstruction method invoked by the [Scanalyze](http://graphics.stanford.edu/software/scanalyze)
     software package used in the [Digital Michelangelo Project](http://graphics.stanford.edu/projects/mich).
      Another software package that might be of interest is [Volfill](http://graphics.stanford.edu/software/volfill), our diffusion-based hole filler
       for large polygon meshes.

The second set of models below were acquired at a XY scan resolution of 100 microns using the [XYZ RGB](http://www.xyzrgb.com/) 
auto-synchronized camera, which is based on technology developed in the [Visual Information Technology](http://iit-iti.nrc-cnrc.gc.ca/about-sujet/vit-tiv_e.html)
 group of the Canadian National Research Council (NRC). This camera has an accuracy (3 Sigma) of 
 ± 0.025mm (±0.001"), and X, Y, and Z-axis resolutions of 0.1mm (0.004"), 0.002mm (0.00008"), and 
 0.003mm (0.0001"), respectively, as determined using a DEA Scirocco coordinate measuring machine. 
 All post-processing, including alignment, merging, editing, and polygon reduction, were done using
  [Innovmetric](http://www.innovmetric.com/)'s Polyworks software. These models come to us courtesy of Helmut Kungl.

##### File format

Unless otherwise noted, the range data and reconstructed models in this repository are stored in PLY 
files. This format was developed at Stanford University, and the source code is available for [download](http://graphics.stanford.edu/pub/zippack/ply-1.1.tar.Z).
 For convenience, we have represented most of these PLY files in their ASCII formats. Choosing ASCII makes it possible for someone unfamiliar with it to get a feel for the file format, and it avoids the problem of using the correct big-endian vs. little-endian byte orders.
To view PLY files, you can download our [Scanalyze](http://graphics.stanford.edu/software/scanalyze) software package. For converting PLY files to other formats, here are some converters we have or know about:

- Our utility for converting PLY files to Inventor files. Click [here](http://graphics.stanford.edu/data/3Dscanrep/ply2iv) to download the executable.
- [Richard Harding](Richard_Harding@Playstation.sony.com) of the Sony Playstation group has contributed a [ply-to-Maya plugin](http://graphics.stanford.edu/data/3Dscanrep/plyImportExport_1.2.zip).
 It supports import from PLY to Maya, and export from Maya to PLY, for versions 6.0 and 7.0 of Maya. Starting with Maya 8.5, 
 this exporter can be downloaded from [here](https://sites.google.com/site/mayaplyimportexport/).
- [Bruce Merry)(bmerry@cs.uct.ac.za) of South Africa has written a script to import PLY files to Blender. Click [here](http://wiki.blender.org/index.php/Extensions:Py/Scripts/Manual/Import/PLY) to download it.
- A [shareware program](http://web.axelero.hu/karpo) written by Zoltan Karpati for converting between many 3D formats, including PLY.
- For converting PLY to OBJ/3DS formats, there used to be a free demo version of Deep Exploration, available [here](http://www.righthemisphere.com/),
 but we hear it is no longer available.
- Diego Nehab (Princeton) has also written a [toolkit for manipulating PLY files](http://www.cs.princeton.edu/~diego/professional/rply).
- Another site with information about PLY files is the [PLY File Format page](http://www.cc.gatech.edu/projects/large_models/ply.html) of 
the Georgia Institute of Technology's [Large Geometric Models Archive](http://www.cc.gatech.edu/projects/large_models).
- Joao Oliveira of University College London has modified the Georgia Tech libraries so that reading of PLY files is robust to the line 
breaks inserted when editing them on various platforms. Here is his [package](http://www.cs.ucl.ac.uk/staff/Joao.Oliveira/ply.html).
- Okino's PolyTrans package includes a PLY [importer](http://www.okino.com/conv/imp_ply.htm) and [exporter](http://www.okino.com/conv/exp_ply.htm).
- Paolo Cignoni's MeshLab system, available from [SourceForge](http://meshlab.sourceforge.net/).
- A C++ library for parsing PLY files, written by Ares Lagae, is available [here](http://www.cs.kuleuven.ac.be/~ares/libply/). 

We have not tested any of these converters ourselves. Feedback or bug reports should be sent directly to the authors of these packages.

##### Contacting us

For questions and comments about our archive, send mail to:

    scanrep-question at graphics dot stanford dot edu 

To subscribe to the 3D Scanning Repository's email list, send mail to:

    majordomo@lists.stanford.edu 

with the message body:

    subscribe graphics-scanrep-announce 

##### Please acknowledge...

Please be sure to acknowledge the source of the data and models you take from this repository. In each of the listings below, we have cited the source of the range data and reconstructed models. You are welcome to use the data and models for research purposes. You are also welcome to mirror or redistribute them for free. Finally, you may publish images made using these models, or the images on this web site, in a scholarly article or book - as long as credit is given to the Stanford Computer Graphics Laboratory. However, such models or images are not to be used for commercial purposes, nor should they appear in a product for sale (with the exception of scholarly journals or books), without our permission.

##### Inappropriate uses of these models

As you browse this repository and think about how you might use our 3D models and range datasets, please remember that several of these artifacts have religious or cultural significance. Aside from the buddha, which is a religious symbol revered by hundreds of millions of people, the dragon is a symbol of Chinese culture, the Thai statue contains elements of religious significance to Hindus, and Lucy is a Christian angel; statues like her are commonly seen in Italian churches. Keep your renderings and other uses of these particular models in good taste. Don't animate or morph them, don't apply Boolean operators to them, and don't simulate nasty things happening to them (like breaking, exploding, melting, etc.). Choose another model for these sorts of experiments. (You can do anything you want to the Stanford bunny or the armadillo.)   
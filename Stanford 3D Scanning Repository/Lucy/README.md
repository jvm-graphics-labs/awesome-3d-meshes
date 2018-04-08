# Lucy

![image](http://graphics.stanford.edu/data/3Dscanrep/lucy-vray_28_mil_poly_hdri_gi.gif)

Source: Stanford University Computer Graphics Laboratory
Scanner: [Stanford Large Statue Scanner](http://graphics.stanford.edu/projects/mich/mgantry-in-lab/mgantry-in-lab.html)
Number of scans: 47
Total size of scans: 58,241,932 points (approx 116 million triangles)
Reconstruction: vrip at 0.5 mm, holefilling
Size of reconstruction: 14,027,872 vertices, 28,055,742 triangles
Comments: hole-free, but contains small bridges due to space carving, so its topological genus is larger than it appears.
It may also have a few topological problems, making it not a proper manifold. Thanks to the [Chaos Group](http://www.chaosgroup.com/) for the rendering above.

Range data:
    lucy_scans.tar.gz ( SD format; 155 MB compressed, 325 MB uncompressed)

    Note about this range dataset: Lucy was scanned on two separate occasions. The raw range data (lucy_scans.tar.gz) and the VRIPped reconstruction (lucy.tar.gz) unfortunately do not correspond to the same scan of the statue. Moreover, the raw range data was never aligned, so the *.xf transform files in lucy_scans.tar.gz (as well as those in lucysd.tar.gz in the same directory) do not register the scans together. 

Vripped reconstruction:
    lucy.tar.gz (307 MB compressed, 508 MB uncompressed)

    A QSplat version of this model is available in the [QSplat models archive](http://graphics.stanford.edu/data/qsplat/). 

Using Lucy: Please remember that Lucy is a Christian angel. See our reminder above about [inappropriate uses] of this model.
Feel free, however, to build a [lego replica](http://graphics.stanford.edu/data/3Dscanrep/lucy-lego-s.jpg) of Lucy, 
as David Winkler has done. Check out his explanation of the [conversion process](http://www.brickshelf.com/gallery/happyfrosh/BrickFest2005/automatedbricklayout.pdf). 
You can also download the [plans](http://www.brickshelf.com/gallery/happyfrosh/StanfordAngel/) and build it yourself.   
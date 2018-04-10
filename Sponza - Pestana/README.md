# [Base color, Roughness and Metallic textures for Sponza](http://www.alexandre-pestana.com/pbr-textures-sponza/)

> It’s been a long time since my last blog post, mainly because I’m currently “stuck” on non graphic work. I started to work on an
 editor to be able interact more easily with objects in my engine, a socket class to handle the communications between the editor and
  the engine, and mechanisms to handle auto generated code. Maybe I will write a blog post on this when it will be up and running, 
  for now it’s mainly tests, researchs and prototypes.
>
> Anyway, few weeks ago I decided to start using PBR in my engine. I used the same equations as in my [PBR viewer](http://www.alexandre-pestana.com/disney-principled-brdf-implementation/)
, so it wasn’t really complicated to implement. In fact the part that took me most of the time was creating the Base Color, Normal, 
Roughness and Metallic textures for each materials in Sponza, so I thought it might worth sharing it if it can save someone some time. 
I used the textures provided as base, and created the missing ones with [Substance Designer](http://www.allegorithmic.com/products/substance-designer). So that’s why I should use “PBR” with quotes, the textures are far from being calibrated or scanned, it was mainly made to look ok and being able to test a quick PBR environnement. And I’m not an artist, so It may be better to consider this as “programmer art”.
> ![Image](http://alexandre-pestana.com/wordpress/wp-content/uploads/2015/02/SponzaPBR-1024x554.png)
> Sponza in my engine with the new textures
>  
>  All the textures are 1024×1024. For those who would like to use this as base to create more accurate textures I also uploaded the substance file with all the graphs I used to create those textures. And if you want to convert the textures to a specular workflow it would be really easy to do as well.
> ![Image](http://alexandre-pestana.com/wordpress/wp-content/uploads/2015/02/Substance-1024x750.png)
> If you want to use the mtl file, I stored the metallic textures in the “map_Ka” channel, and the roughness in “map_Ns”.
>  
>  I don’t put any restriction on the use of those new textures, but the original  textures were made by [Frank Meinl](http://www.crytek.com/cryengine/cryengine3/downloads) 
and modified by [Morgan McGuire](http://graphics.cs.williams.edu/data/meshes.xml), and you will find the proper copyright file included.
> ![Image](http://alexandre-pestana.com/wordpress/wp-content/uploads/2015/02/SponzaPBR2-1024x548.png)
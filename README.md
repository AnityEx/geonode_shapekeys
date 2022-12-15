**geonode_shapekeys**
==============
add shapekeys to override rigs, copied from blender repository for personal use (https://developer.blender.org/diffusion/BSTS/browse/master/geonode-shapekeys/geonode_shapekeys/) original licence is cc-by in blender cloud (https://studio.blender.org/films/charge/3aee478ba5e53a/?asset=6243)


description from blender cloud:

*"You can't create shape keys on linked meshes in current Blender, even with the awesome new override system, overriding per-vertex data like shape keys or vertex groups is not possible. However, it is possible to add modifiers. And GeoNodes is a modifier. So, we threw the problem at Simon, he gave me some nodes, I wrote some Python operators and UI, and it seems like we now have shape keys on linked meshes.***

*Although it seems in some cases there's some precision issues (as you can see on the mouth corner), maybe we can fix that later. Also, the modifier has to come AFTER any existing modifiers in the stack, which may be an issue in some cases.*

*This is now included in the Blender Studio Tools repository under "GeoNode Shape Keys", but we haven't used it in production yet because we came up with it when most of the movie was already done, so consider it unbaked for now."*


from blender repository:

**GeoNode Shape Keys**

*GeoNode Shape Keys is a Blender Add-on that lets you deform linked and overridden meshes using sculpt mode in a roundabout way using a geometry node set-up. While the current override system doesn't support adding or editing shape keys on overridden meshes, it does allow you to add modifiers, so this add-on leverages that.*

Installation
==============
Download this repository as zip. install zip as any blender addon



How to use
==============
The add-on's UI is only visible on linked and overridden meshes. It can be found under Properties->Object Data->Shape Keys->GeoNode Shape Keys. The add button will do the following:

Create a local version of the evaluated object that you can sculpt on
Create a modifier on the linked object, that will apply your sculpted changes to it
After creating a set-up, you get a button to conveniently swap between the two objects.

Removing a list entry should also remove the relevant modifier and object. Otherwise, it will throw a warning.

The node set-up that applies the deformation relies on a UV map.

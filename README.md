In the time I've talked to you, a lot of things have changed.  We have learned that the size of the showroom we'll be working in is actually a lot smaller than we were initially led to believe.  We are now able to only to map one half of the car.  That actually allows us to do some more forced perspective illusions with the audience, so the fluid simulations are more feasible.  Initially, I was thinking the best thing to do would be to have the balls fall onto the mesh of the car and roll along the surface, but now that we'll have the bodies corralled into one perspective, I'd like to fill the vehicle from the inside.  We'll be viewing the car from the drivers side, with a 1080 screen behind the vehicle.  The screen is going to be used to help simulate movement using passing landscapes. 

The main inspiration that we're using on this project is work by Vincent Houze.  His work can be found at https://vimeo.com/foliativ

He has edited a C++ CHOP in Touchdesigner and released it as the flex CHOP. https://github.com/vinz9/FlexCHOP

I have deactivated my commercial license on touchdesigner 099.
Login: scott@2baysdjs.com
Password: Password1

We had a bit of trouble when we went to compile, but we just had to relocate a cuda file.  I'm sure you'll have no trouble.

Once inside, you'll see there is a volume box in the top left.  Below that, the emitter is created.

On the bottom left are the collider boxes and spheres.
The boxes are created using the CHOP data t[xyz] ans s[xyz].  In this case, it's two constant CHOPs merging.  The interesting thing about this method, is the C++ CHOP uses the CHOP data, and then seperately there is a SOP created and rendered to appear as if they are bouncing off of a mesh.  When I insert the Porsche model into the Geometry comp, the particles still react to the boxes, but the car appears in my render.

In the middle of the network is the C++ CHOP, renamed flexCHOP.  There are custom parameters created to mess with all sorts of variables, gravity, viscosity, etc.  It does the heavy lifting and creates all of the points for the particles to be instanced.

A GLSL shader is impemented on all of the instanced geometry and rendered out in the render1 TOP.

In the time I've talked to you, a lot of things have changed.  We have learned that the size of the showroom we'll be working in is actually a lot smaller than we were initially led to believe.  We are now able to only to map one half of the car.  That actually allows us to do some more forced perspective illusions with the audience, so the fluid simulations are more feasible.  Initially, I was thinking the best thing to do would be to have the balls fall onto the mesh of the car and roll along the surface, but now that we'll have the bodies corralled into one perspective, I'd like to fill the vehicle from the inside.  We'll be viewing the car from the drivers side, with a 1080 screen behind the vehicle.  The screen is going to be used to help simulate movement using passing landscapes.

Inside the drive is an FBX file for the

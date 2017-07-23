![materials/editor/env_fog_controller.png](http://i.imgur.com/pzIIysQ.png)

Example Fog Gradient:
![materials/effects/example_gradient_fog.png](http://i.imgur.com/prOKgZE.png)

## steamtours.fgd
```java
@PointClass
	iconsprite( "materials/editor/env_fog_controller.vmat" )
	base( Targetname )
	gradientfog()
= env_gradient_fog
[
	fogstart(float) : "Fog Start Distance" : "0.0"
	fogend(float) : "Fog End Distance" : "4000.0"
	fogstartheight(float) : "Fog Start Height" : "0.0"
	fogendheight(float) : "Fog End Height" : "200.0"
	farz(string) : "Far Z Clip Plane" : "-1"
	gradientfogtexture(resource:texture) : "Fog Gradient Texture" : "materials/effects/example_gradient_fog.vtex"
]
```
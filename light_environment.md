Formerly light_directional, part of the VR forward lighting system, eventually replaced the old light_environment.

![](http://i.imgur.com/74UcNIE.png)

```java
@PointClass
	light()
	base(light_base, light_base_legacy_params)
	editormodel("models/editor/sun")
	global( sun )
	bakeskylight( skycolor, skyintensity, lower_hemisphere_is_black, skytexture )
	bakeambientocclusion( ambient_occlusion, max_occlusion_distance, fully_occluded_fraction, occlusion_exponent )
	bakeambientlight( ambient_color )
	= light_environment :  "Sets the color and angle of the light from the sun and sky."
[
	angulardiameter(float) : "SunSpreadAngle" : "5.0" : "The angular extent of the sun for casting soft shadows. Higher numbers are more diffuse. 5 is a good starting value."

	numcascades(integer) [ group = "Shadows" ] : "Cascade Count" : 3 : "Number of shadow cascades to use."
	shadowcascadedistance0(float) [ group = "Shadows" ] : "Cascade Distance 0" : "0.0"
	shadowcascadedistance1(float) [ group = "Shadows" ] : "Cascade Distance 1" : "0.0"
	shadowcascadedistance2(float) [ group = "Shadows" ] : "Cascade Distance 2" : "0.0"
	//shadowcascadedistance3(float) [ group = "Shadows" ] : "Cascade Distance 3" : "0.0"
	shadowcascaderesolution0(integer) [ group = "Shadows" ] : "Cascade Resolution 0" : 0
	shadowcascaderesolution1(integer) [ group = "Shadows" ] : "Cascade Resolution 1" : 0
	shadowcascaderesolution2(integer) [ group = "Shadows" ] : "Cascade Resolution 2" : 0
	//shadowcascaderesolution3(integer) [ group = "Shadows" ] : "Cascade Resolution 3" : 0

	skycolor(color255) [ group = "Sky" ] : "Sky Color" : "255 255 255"
	skyintensity(float) [ group = "Sky" ] : "Sky Intensity" : "1.0"
	lower_hemisphere_is_black(boolean) [ group = "Sky" ] : "Lower Hemisphere Is Black" : "1"
	skytexture(target_destination) [ group = "Sky" ] : "Sky IBL Source" : "" : "env_sky entity, lat-long/h-cross/v-cross skybox image, or sky material to use for sky IBL"

	ambient_occlusion(boolean) [ group = "Ambient Occlusion" ] : "Ambient Occlusion" : "0"
	max_occlusion_distance(float) [ group = "Ambient Occlusion" ] : "Ambient Occlusion Max Distance" : "80.0"
	fully_occluded_fraction(float) [ group = "Ambient Occlusion" ] : "Ambient Occlusion Fully Occluded Fraction" : "1.0"
	occlusion_exponent(float) [ group = "Ambient Occlusion" ] : "Ambient Occlusion Exponent" : "1.0"

	ambient_color(color255) [ group = "Ambient Light" ] : "Ambient Lighting" : "0 0 0"
]
```
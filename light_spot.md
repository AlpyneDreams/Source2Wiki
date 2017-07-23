![light_spot](http://i.imgur.com/377TyDC.png)

```java
@PointClass
  light()
  base(light_base, light_base_legacy_params, light_base_attenuation_params, CanBeClientOnly)
  editormodel("models/editor/spot")
  leansphere(lightsourceradius,255,255,255)
  lightcone()
  = light_spot : "A spot light source."
[
	lightcookie(string) : "Light Cookie" : "" : "light cookie name in effects/lightcookies.vtex"

	falloff(float) : "Falloff" : "1" : "angular falloff exponent for spot lights"
	innerconeangle(float) : "Inner Cone Angle" : "45" : "inner cone angle. no angular falloff within this cone"
	outerconeangle(float) : "Outer Cone Angle" : "60" : "outer cone angle"

	shadowfademindist(float) : "Shadow Start Fade Dist" : -250 : "Distance at which the shadow starts to fade (<0 = use fademaxdist)."
	shadowfademaxdist(float) : "Shadow End Fade Dist" : 1000 : "Maximum distance at which the shadow is visible (0 = don't fade out)."
]
```
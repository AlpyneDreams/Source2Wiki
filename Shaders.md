```yaml
aerial_perspective:
  Applies Rayleigh scattering to simulate the appearance of far away objects through atmospheric scattering
apply_fog:
  Apply accumulated fog to the opaque rendered objects
bilateral_blur:
  Used to apply a two-pass separable box blurring filter to an image
bink:
  Used to draw bink movies
black:
  Cheap shader that just outputs black (with fog)
blend:
  Blend Shader for world surfaces
bloom:
  Bloom downsample, shape, and blur
blur:
  RGB blur using one of 4 Gaussian kernels
brushsplat:
  Shader that lets you blend lots of textures together over a surface
cables:
  Cables shader used for particle system cables
celestial_body:
  Shader used to draw celestial bodies in the skybox with a particle system
convolve_environment_map:
  Blurs cubemap faces according to the GGX specular term.
copytexture:
  Copy texture
$debug:
  debug_sh_visualization:
    Used to inject point light sources into a light propagation volume
  debug_show_texture:

  debug_sunshadow_vis:
    Used to visualize the cascaded shadow map split boundaries
  debug_wireframe_2d:
    Simple, no frills screenspace wireframe with per-vertex colors
  debugoverlay_wireframe:
    Wireframe for tools
deferred_shading:
  Tiled Deferred Shading
depth_only:
  Depth Only - Used as a Mode Fallback
depth_only_foliage:
  Depth Only - Used as a Mode Fallback
downsample:
  Shader to downsample rendertargets
error:
  Error shader
fogsprite:
  Shader used to render volumetric fog particles
fogtonemapsrgb:
  Computes a local ambient occlusion (AO) term using the g-buffer
foliage:
  Foliage shader with animation
gaussian_bloom_blur:
  Screenspace Reflections Blur
general_filter:
  Shader used form performing various 2d convolutions.
generic:
  Shader that is used for tools helper materials in core
generic_light:
  Used to accumulate lighting for light geometry
glass:
  A glass shader.
gradient_aa_lines:
  Gradient Antialiased Lines Shader
grasstile:
  Grass Shader
grasstile_preview:
  Standard shader for all non-blend surfaces
hdr_post_process:
  HDR Tonemapping and Postprocessing
height_fog:
  Accumulate fog density from a ground-plane-based fog volume
imageformat_test:
  Used for rendersystemtest imageformattest
irradiance_volume:
  Used to splat irradiance volume lighting into the world
$light_propagation_volumes:
  light_propagation_volume:
    Used to splat light propagation volume lighting into the world
  light_propagation_volume_accumulate:
    Used to accumulate intermediate LPV propagation passes to final result using additive blending
  light_propagation_volume_fixup:
    Used to inject point light sources into a light propagation volume
  light_propagation_volume_injection:
    Used to inject point light sources into a light propagation volume
  light_propagation_volume_propagation:
    Used to inject point light sources into a light propagation volume
minimap_fow:
  Used to draw fog of war on the minimap
morph_composite:
  Composite morph texture
$occlusion:
  occluder_depth_overlay:
    Occluder Depth Overlay
  occluder_vis:
    Shader to visualize occluder geometry
  occlusion:
    Shader used by occlusion query proxy rendering
$panorama:
  panorama:
    Used for Panorama UI
  panorama_fancyquad:
    Used for panorama fancy quad
  panorama_test:
    Used for rendersystemtest panoramatest
parallax_occlusion:
  Parallax Occlusion Mapping test material
physics_wireframe:
  Wireframe for physics model visualization
post_process:
  Post processing
$decals:
  projected_decal_modulate:
    Projected modulated decal
  projected_decals:
    Projected decals
  projected_sheet_decals:
    Projected decals (VR)
reconstruct_normals:
  Creates a buffer of normals reconstructed from depth while performing nearest-filtered downsampling of depth.
refract:
  Refraction
sampletexture_bicubic:
  Shader that scales input texture using bicubic filtering
screen_texture_with_depth:
  Used to draw screen space textures at a specific depth
$screenspace_reflections:
  screenspace_reflections:
    Screenspace Reflection Shader
  screenspace_reflections_blur:
    Screenspace Reflections Blur
$sfm:
  sfm_accumulation:
    Shader used by the SFM's accumumation buffer
  sfm_hsl_grain:
    Shader used by the SFM's CDmeHSLGrainFXClip
  sfm_textured_unlit:
    Unlit Textured With Depth
  sfm_volumetrics_frustum:
    Shader used by the SFM's volumetric lights
simple:
  Simple shader to use as a starting point for writing new shaders
simple_water:
  Standard shader you should use on everything for now
$sky:
  sky:
    Used to draw the skybox
  sky_lighting:
    Sample lighting from sky paraboloid map
  sky_model:
    Implementation of 'An Analytic Model for Full Spectral Sky-Dome Radiance' presented by Lukas Hosek and Alexander Wilkie of Charles University in Prague in SIGGRAPH 2012.
solidcolor:
  A shader for untextured and unlit meshes
spritecard:
  Shader used by the particle system
spriteentity:
  Shader used by env_sprite
$ssao:
  ssao:
    Computes a local ambient occlusion (AO) term using the g-buffer
  ssao_bilateral_blur:
    Scalable Ambient Obscurance Bilateral Blur
  ssao_convert_depth:
    Scalable Ambient Obscurance Depth Conversion
  ssao_downsample_depth:
    Scalable Ambient Obscurance Depth Downsample
  ssao_scalable_ambient_obscurance:
    Scalable Ambient Obscurance AO computation
sunlight:
  Used on opaque objects for rendering into parallel split shadow buffers
tonemap_query:
  Compares the luminance against a constant value and returns all 1's when greater
$tools:
  tools_2d_generic:
    Screenspace, per-vertex color, (optionally) textured
  tools_encode_environment_map:
    Performs essential processing on cube map faces.
  tools_generic:
    Tools Generic
  tools_light_probe:
    Shader used in tools to render the reflection from an environment map. Meant to look like Paul Debevec's light probes. See www.debevec.org/probes
  tools_modelviewer_wireframe:
    Debug shader that renders wireframe for model viewer
  tools_selection_overlay:
    Selection overlay
  tools_solid:
    Solid/stripes/checkerboard for tools
  tools_solid_color:
    Solid color
  tools_sprite:
    Point rendering for tools
  tools_textured_unlit:
    Unlit Textured
  tools_visualize_collision_mesh:
    Debug shader to visualize collision meshes
  tools_visualize_tangent_frame:
    Debug shader that render normals or tangent space as lines
  tools_wireframe:
    Wireframe for tools
ui:
  Used to draw UI elements
unlit:
  Used to draw UI elements
upsampleindirect:
  Computes a local ambient occlusion (AO) term using the g-buffer
$visualization:
  visualize_depth:
    Expensive shader to visualize a depth texture
  visualize_nav:
    Simple shader to use as a starting point for writing new shaders
  visualize_physics:
    Simple shader to use as a starting point for writing new shaders
$volumetric_fog:
  volumetric_fog_apply:
    Applies volumetric fog to each pixel on screen
  volumetric_fog_create_density:
    Applies volumetric fog to each pixel on screen
  volumetric_fog_integrate:
    Integrates volumetric fog from front to back of the volume
$vr:
  vr_depth_only:
    VR Depth Only - Used as a Mode Fallback
  vr_eyeball:
    Eyeballs
  vr_monitor:
     Style Monitor Shader
  vr_shatterglass:
    Shatterglass
  vr_simple:
    Diffuse-only shader with no normal maps
  vr_skin:
    Shader for skin/flesh materials
  vr_skin_blended:
    Shader for skin/flesh materials - Allows you to blend between different types of skin
  vr_standard:
    Standard shader for surfaces that require normal maps
  vr_stencil:
    Shader used for rendering stencil pattern to mask pixels user can't see through lenses
  vr_substance_painter:
    Substance Painter shader - Should render objects as they appear in substance painter
  vr_unlit:
    Unlit shader
  vr_warp:
    Shader used for warping each stereo view for lens correction
  vr_wormhole:
    Shader for wormhole teleportation effect
warp_test:
  Test shader for testing 'extra shader data' functionality in sceneobjects.
water:
  Water
```
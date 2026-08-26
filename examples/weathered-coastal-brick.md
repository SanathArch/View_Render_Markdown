---
base_view_id: "coastal-brick-facade-01"
name: "Weathered Coastal Brick Facade — Golden Hour"
version: "1.0"
status: locked
project: "View_Render_Markdown / worked example"
author: "Sanath"
date_created: "2026-08-26"
last_updated: "2026-08-26"
tags: [architecture, coastal, brick, golden-hour, weathering]
derived_views: []

render_type: cgi
render_style: photoreal
engine: "V-Ray (or Octane equivalent)"
render_method: "path tracing"
sampler_or_gi:
  samples_or_steps: "2048 spp"
  gi_bounces: 6
  denoiser: "OIDN, light strength"
  cfg_scale: ""
color_management:
  working_space: ACEScg
  view_transform: "ACES 1.0 SDR-video"
  bit_depth: "32-bit float, delivered 16-bit"
output:
  resolution: "4096x2731"
  aspect_ratio: "3:2"

camera:
  body_reference: "full-frame mirrorless, ~50MP equiv."
  sensor_size: "full-frame 36x24mm"
  lens:
    focal_length_mm: 35
    type: prime
    character: "modern, clean coatings, slight natural falloff"
    aperture_f: 5.6
  focus:
    focus_distance_m: 4.5
    depth_of_field: "moderate — facade fully sharp, foreground planter softly out of focus"
  exposure:
    shutter_speed: "1/250s"
    iso: 100
    white_balance_k: 5200
  framing:
    height_m: 1.6
    distance_to_subject_m: 5
    angle: "eye-level, slight upward tilt (~5°) to include roofline"
    field_of_view_deg: 54.4
  lens_artifacts:
    distortion_pct: 0.5
    vignetting: "subtle, natural falloff at corners"
    chromatic_aberration: "minimal, faint on brightest window highlights"

lighting:
  primary_source: sun
  time_of_day: golden-hour-pm
  sun_altitude_deg: 8
  sun_azimuth_deg: 260
  geo_reference: "coastal Mediterranean town, ~41°N, late September, 18:40 local"
  color_temperature_k: 3200
  sky_condition: "clear, faint haze near horizon"
  intensity_ev: 12.5
  shadows:
    length_relative: "~5x subject height"
    direction: "raking left-to-right across facade, exaggerating mortar joints"
    hardness: "soft-medium — sun low, slight haze diffusion"
    density: "deep but not crushed; open shadow detail from sky fill"
  key_to_fill_ratio: "4:1"
  fill_source: "clear blue sky, opposite the sun"
  rim_or_backlight: "faint warm rim on brick edges facing the sun"
  practical_lights: []
  hdri_reference: "references/images/lighting/coastal-golden-hour-hdri.jpg, rotated to match azimuth 260°"
  volumetrics: "very light haze, barely visible in raking light"

materials:
  - zone: "facade-brick"
    category: stone
    pbr:
      base_color: "#B5624A weathered terracotta, uneven — 15% desaturated/faded variant mixed in"
      roughness: "0.75-0.9, matte, micro-variation between units"
      metallic: 0
      specular_or_ior: 1.5
      normal_detail: "chipped arrises, eroded mortar recess ~3mm"
      height_displacement_mm: 4
      subsurface_scattering: "none significant"
      anisotropy: "none"
      clearcoat: "none"
      opacity_translucency: "opaque"
    texture:
      resolution: "4K tiling + 2K unique dirt/damage overlay"
      real_world_scale: "1px ≈ 1.5mm"
      tiling: "brick-course tile, 2m repeat, broken up with unique overlay"
    aging:
      age_category: weathered
      weathering_types:
        - type: uv-fade
          intensity_pct: 40
        - type: grime
          intensity_pct: 25
        - type: efflorescence
          intensity_pct: 15
        - type: cracking
          intensity_pct: 10
      wear_distribution: "efflorescence concentrated at base (rising damp), grime streaking downward from window ledges, uniform UV fade on sun-facing courses"
      causal_environment: coastal-salt
      years_of_exposure_implied: "~60-80 years"
    reference_image: "references/images/materials/coastal-brick-closeup-01.jpg"

  - zone: "window-frame-steel"
    category: metal
    pbr:
      base_color: "#2E2B27 near-black paint, rust bleeding through at seams"
      roughness: "0.55 paint / 0.4 exposed rust patches"
      metallic: "0 painted areas / 0.7 exposed rust"
      specular_or_ior: 1.4
      normal_detail: "paint alligatoring/crazing, pitted corrosion at joints"
      height_displacement_mm: 1
      subsurface_scattering: "none"
      anisotropy: "none"
      clearcoat: "none, paint sheen fully degraded to matte"
      opacity_translucency: "opaque"
    texture:
      resolution: "2K"
      real_world_scale: "1px ≈ 1mm"
      tiling: "unique, no tiling"
    aging:
      age_category: derelict
      weathering_types:
        - type: rust
          intensity_pct: 35
        - type: peeling
          intensity_pct: 30
        - type: water-staining
          intensity_pct: 20
      wear_distribution: "rust blooms below every bolt head and hinge — rainwater channels there; peeling concentrated on sun-facing (south) side"
      causal_environment: coastal-salt
      years_of_exposure_implied: "~40 years, unmaintained ~15"
    reference_image: "references/images/materials/steel-frame-rust-01.jpg"

composition:
  aspect_ratio: "3:2"
  technique: "rule-of-thirds — facade fills right two-thirds, planter foreground anchors bottom-left third"
  layering: "fg: terracotta planter (soft focus) / mg: brick facade with window / bg: sliver of sky, warm and clear"
  negative_space: "sky negative space top-left, ~15% of frame"
  horizon_position: "not visible — facade fills frame edge to edge vertically"

grade:
  style_reference: "warm film emulation, restrained — not a heavy teal-orange split"
  lut_reference: "references/images/composition/grade-ref-warm-film.jpg"
  contrast_curve: "gentle S-curve, lifted shadows"
  black_point: 8
  white_point: 245
  saturation: "+6% overall, -10% on blues to keep sky from competing with brick"
  grain: "fine, ISO-200-film equivalent"
  bloom: "very subtle on direct sun-hit brick edges"
  post_vignette: "barely-there, 5%"

environment:
  location_type: exterior
  season: "early autumn"
  weather: "clear"
  atmosphere: "faint coastal haze near horizon only"
  time_period: contemporary
---

# Weathered Coastal Brick Facade — Golden Hour

A single ground-floor facade of a ~80-year-old coastal building, shot at low sun angle to rake light across the
brick and dramatize the eroded mortar joints and rusted window steel. This is the reference "weathered masonry"
base view for the project — any future coastal/aged-brick shot should diff against this one rather than starting
from scratch.

## Sun & Lighting Notes

Sun altitude of 8° was chosen specifically because anything higher flattens the mortar-joint relief that makes
old brickwork read as old — raking light at this angle is what separates "brick texture visible" from "brick
texture merely implied by color." Azimuth 260° puts the light source just off-camera-left, so the facade's right
edge catches a warm rim while the left third falls into soft, sky-filled shadow. Color temperature at 3200K is
warmer than the "golden hour" default of ~3500-4000K — pushed further because the reference photos this was
matched against were shot closer to true sunset than mid-golden-hour.

## Material & Aging Notes

**Brick:** The building faces the harbor, so efflorescence (the white mineral bloom from rising damp) is
concentrated in the bottom third of the facade, not evenly distributed — salt-laden groundwater wicks up through
the porous brick and evaporates, leaving mineral deposits. UV fade is closer to uniform since the facade gets
consistent afternoon sun, but grime deliberately streaks *downward* from window ledges, following the path
rainwater actually takes rather than being painted on as a flat dirt layer.

**Steel window frame:** Rust is not random — it blooms specifically below every bolt head and hinge, because
that's where water collects and paint fails first. The south-facing side (sun-hit, more thermal cycling) shows
more paint peeling than the shaded side. This causal logic is what should be reused on any similar coastal-steel
zone: rust and peeling follow water and heat, not an even "aged" noise pattern.

## Reference Images

| Aspect | Reference | Notes |
|---|---|---|
| Lighting | `references/images/lighting/coastal-golden-hour-hdri.jpg` | match raking angle + warm color temp |
| Material — brick | `references/images/materials/coastal-brick-closeup-01.jpg` | match mortar erosion depth |
| Material — steel frame | `references/images/materials/steel-frame-rust-01.jpg` | match bolt-head rust blooms |
| Aging | `references/images/aging/efflorescence-base-course.jpg` | rising-damp pattern at base course |
| Composition | `references/images/composition/grade-ref-warm-film.jpg` | overall color/mood target |

*(Reference image files themselves are not yet dropped into these folders — the paths above are the naming
convention to follow when they are.)*

## Open Questions

- Should the planter foreground be its own material block, or is "soft focus, out of scope" sufficient given it's never in sharp focus?
- Confirm 3200K isn't overshooting — compare against a second real photo reference before locking further variants.

## Revision Log

| Date | Change | Author |
|---|---|---|
| 2026-08-26 | Initial fully-populated worked example, status set to locked | Sanath |

---
# ============================================================
# BASE VIEW — identity
# ============================================================
base_view_id: ""                # short slug, e.g. "coastal-brick-facade-01"
name: ""                        # human title
version: "0.1"
status: draft                   # draft | approved | locked
project: ""
author: ""
date_created: ""                # YYYY-MM-DD
last_updated: ""                # YYYY-MM-DD
tags: []                        # e.g. [architecture, coastal, brick, golden-hour]
derived_views: []                # shots/variants that inherit this base view + only record their deltas

# ============================================================
# RENDER STYLE & PIPELINE
# ============================================================
render_type: ""                  # photograph | cgi | ai-generated | hybrid
render_style: ""                 # photoreal | cinematic | editorial-product | documentary | hyperreal
engine: ""                       # Octane / V-Ray / Redshift / Corona / Arnold / Cycles / UE5 Path Tracer
                                  #   -- or, for AI generation: Midjourney v6 / SDXL / Flux / Nano Banana + model/checkpoint
render_method: ""                # path tracing | ray tracing + baked GI | diffusion sampling
sampler_or_gi:
  samples_or_steps: ""           # render samples, OR diffusion steps
  gi_bounces: ""
  denoiser: ""
  cfg_scale: ""                  # diffusion only — leave blank for CGI/photo
color_management:
  working_space: ""              # ACEScg / linear sRGB / Display P3
  view_transform: ""             # Filmic / AgX / Standard / ACES sRGB
  bit_depth: ""                  # 8-bit SDR / 16-bit / 32-bit float HDR
output:
  resolution: ""                 # e.g. 4096x2731
  aspect_ratio: ""                # e.g. 3:2

# ============================================================
# CAMERA
# ============================================================
camera:
  body_reference: ""             # e.g. "full-frame mirrorless, ~61MP" / "medium format"
  sensor_size: ""                 # full-frame 36x24mm / APS-C / medium format / virtual-35mm
  lens:
    focal_length_mm: ""
    type: ""                     # prime | zoom
    character: ""                # vintage glow / clinical modern / anamorphic
    aperture_f: ""
  focus:
    focus_distance_m: ""
    depth_of_field: ""           # shallow / moderate / deep — describe bokeh quality if shallow
  exposure:
    shutter_speed: ""
    iso: ""
    white_balance_k: ""          # camera white balance setting, distinct from scene light color temp
  framing:
    height_m: ""                 # camera height off ground
    distance_to_subject_m: ""
    angle: ""                    # eye-level / low-angle / high-angle / dutch-<deg> / bird's-eye / worm's-eye
    field_of_view_deg: ""
  lens_artifacts:
    distortion_pct: ""
    vignetting: ""
    chromatic_aberration: ""

# ============================================================
# LIGHTING & SUN POSITION
# ============================================================
lighting:
  primary_source: ""             # sun / overcast-sky / studio-strobe / practical / mixed
  time_of_day: ""                 # golden-hour-am / golden-hour-pm / blue-hour / high-noon / overcast / night
  sun_altitude_deg: ""            # 0-90 above horizon
  sun_azimuth_deg: ""             # compass bearing of light direction
  geo_reference: ""               # lat/long or city + date, for reproducible sun angle
  color_temperature_k: ""
  sky_condition: ""               # clear / hazy / overcast / partly-cloudy
  intensity_ev: ""
  shadows:
    length_relative: ""           # relative to subject height
    direction: ""
    hardness: ""                  # hard / soft, penumbra width
    density: ""                   # how dark/opaque
  key_to_fill_ratio: ""
  fill_source: ""                 # sky bounce / reflector / secondary light
  rim_or_backlight: ""
  practical_lights: []            # list of {name, color_k, intensity, falloff}
  hdri_reference: ""               # path + rotation-deg
  volumetrics: ""                  # haze/fog density, god rays

# ============================================================
# MATERIALS — repeat one block per surface zone
# (see templates/material-block.md for the copy-paste unit)
# ============================================================
materials: []

# ============================================================
# COMPOSITION & FRAMING
# ============================================================
composition:
  aspect_ratio: ""
  technique: ""                   # rule-of-thirds / golden-ratio / leading-lines / framing-device / symmetry
  layering: ""                    # foreground / midground / background notes
  negative_space: ""
  horizon_position: ""

# ============================================================
# COLOR GRADE & POST
# ============================================================
grade:
  style_reference: ""              # teal-orange / bleach-bypass / warm-film / desaturated-documentary
  lut_reference: ""
  contrast_curve: ""
  black_point: ""
  white_point: ""
  saturation: ""
  grain: ""                         # film stock reference + grain size, or noise amount
  bloom: ""
  post_vignette: ""

# ============================================================
# ENVIRONMENT
# ============================================================
environment:
  location_type: ""                 # urban / rural / interior / exterior / studio
  season: ""
  weather: ""
  atmosphere: ""                    # visible fog/haze/humidity
  time_period: ""                   # contemporary / historical-<era> / futuristic
---

# {{ name }}

> One-paragraph description of the shot/scene: what it is, why this base view exists, and what "correct" looks like.

## Sun & Lighting Notes

Prose expansion of the `lighting` block above — why this time of day and sun position were chosen, how the
shadows should read, what the light is doing to the materials in frame.

## Material & Aging Notes

For each surface zone, expand on the structured `materials` entry (see `material-block.md`) with the *story*
of the material: what it's made of, how old it is, what environment aged it, and where the wear concentrates.
This is the section that keeps a render from looking "clean CGI" — be specific about causality, not just
appearance (e.g. "rust blooms below the steel bracket bolts because rainwater channels there" beats "rusty").

## Reference Images

| Aspect | Reference | Notes |
|---|---|---|
| Lighting | `references/images/lighting/...` | what to match, where it's allowed to deviate |
| Material — [zone] | `references/images/materials/...` | |
| Aging | `references/images/aging/...` | |
| Composition | `references/images/composition/...` | |

## Open Questions

- 

## Revision Log

| Date | Change | Author |
|---|---|---|
| | Initial draft | |

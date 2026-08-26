---
base_view_id: "brick-facade"
name: "brick facade"
source_image: "brick-facade.jpg"
source_dimensions: "800×533"
generated: "2026-08-26"
target_model: "nano-banana (image + this spec)"
render_intent: photoreal
output_aspect: "keep"

camera:
  focal_length_mm: 85
  aperture_f: 1.8
  shutter: "1/250"
  iso: 100
  subject_distance_m: 2
  camera_height_m: 1.5
  angle: "eye-level"
  dutch_tilt_deg: 0
  lens_character: "clean modern"
  distortion_pct: 0
  chromatic_aberration_pct: 0
  horizontal_fov_deg: 23.9
  depth_of_field: "6 cm"

lighting:
  time_of_day: "custom"
  sun_altitude_deg: 21
  sun_azimuth_deg: 94
  sun_bearing: "E"
  colour_temperature_k: 5600
  light_rgb: [255, 239, 225]
  sky_condition: "clear"
  key_to_fill_ratio: "7:1"
  fill_source: "sky"
  shadow_direction: "W"
  shadow_length: "2.6× object height"
  shadow_hardness_pct: 88
  atmosphere_haze_pct: 5

grade:
  exposure_ev: 0.2
  contrast_pct: 112
  saturation_pct: 106
  warmth_shift: 22
  shadow_lift_pct: 14
  highlight_rolloff_pct: 55
  grain_pct: 22
  vignette_pct: 18
  bloom_pct: 14

materials:
  - zone: "facade brick"
    category: stone
    surface_pattern: "running-bond brick"
    roughness: 0.65   # matte
    metallic: 0.00
    age_category: weathered
    years_of_exposure: 25
    causal_environment: urban-grime
    wear_distribution: "gravity streaking"
    weathering:
      - type: rust
        label: "Rust / oxidation"
        intensity_pct: 45
      - type: uvfade
        label: "UV fade"
        intensity_pct: 30

scene:
  composition: "rule of thirds"
  location_type: "exterior"
  season: "summer"
  weather: "clear"
  period: "contemporary"

preserve_from_source: ["geometry", "layout", "proportions", "angle", "text"]
---

# brick facade

## Directive

Re-render the attached base image to the specification below.

This is a **relighting and surfacing pass, not a redesign** — hold the source image's geometry, layout, proportions, angle, text exactly as they are and change only light, material, weathering and grade.

Light the scene with a single dominant source at **21° altitude** and **94° azimuth (E)**, colour temperature **5600K**. Cast shadows must run toward **W** at **2.6× object height**, hard-edged with a tight penumbra. Sky is clear; key-to-fill ratio 7:1 with fill coming from sky.

Render through **85mm at f/1.8**, 1/250, ISO 100, focused at 2 m from a camera height of 1.5 m, eye-level angle. Depth of field is very shallow (≈ 6 cm in focus); horizontal field of view 23.9°. Lens character: clean modern.

Grade to a photoreal look: exposure +0.2 EV, contrast 112%, saturation 106%, warmer by 22 units, shadow lift 14%, highlight rolloff 55%, grain 22%, vignette 18%, bloom 14%.

## Lighting

The sun sits **21° above the horizon** on a bearing of **94° (E)**, so every cast shadow in frame runs toward **W** and stretches to **2.6× object height**. Shadow edges are hard-edged with a tight penumbra. This is mid-elevation light — relief is legible without being exaggerated.

Light colour is **5600K** (approx. RGB 255, 239, 225). Sky is **clear**, key-to-fill **7:1**, fill arriving from **sky**. Atmospheric haze at 5% — negligible, the air is clean.

Every shadow in the image must agree with this one light direction. Mismatched shadow directions between objects are the single most common tell of a fake relight.

## Camera

**85mm** at **f/1.8**, 1/250, ISO 100. Camera 1.5 m off the ground, 2 m from the subject, eye-level angle. Horizontal field of view 23.9°; depth of field is very shallow, with roughly **6 cm** acceptably sharp around the focal plane.

Normal perspective — spatial relationships read close to human vision. Lens character: **clean modern**.

## Surfaces, Patterns & Ageing

### facade brick

- **Material:** stone — running-bond brick.
- **Surface response:** roughness 0.65 (matte), metallic 0.00. Treat as a dielectric — specular highlights stay white/neutral over a coloured diffuse base.
- **Age:** weathered, reading as roughly 25 years of exposure under urban grime conditions.
- **Wear:** moderate rust / oxidation (45%), light uv fade (30%).
- **Where the wear sits:** gravity streaking. This distribution is not decorative — concentrate the damage where water, contact and sunlight actually reach, and leave sheltered areas comparatively clean.

## Colour Grade

Exposure +0.2 EV · contrast 112% · saturation 106% · warmth +22 · shadow lift 14% · highlight rolloff 55% · grain 22% · vignette 18% · bloom 14%.

Keep the grade restrained — no single parameter above should announce itself.

## Scene

rule of thirds composition, exterior, summer, clear, contemporary period.

## Hold From The Source Image

- **Geometry** — unchanged from the base image.
- **Layout** — unchanged from the base image.
- **Proportions** — unchanged from the base image.
- **Angle** — unchanged from the base image.
- **Text** — unchanged from the base image.

## Avoid

- Uniformly distributed dirt or noise standing in for weathering — wear follows water, contact and sunlight, never a flat overlay.
- Shadows that disagree with the stated sun bearing (W), or objects with no contact shadow at all.
- Plastic-looking surfaces: an over-smooth normal with no micro-roughness variation reads as CGI regardless of the texture applied.
- HDR halos, over-sharpened edge contrast, or a global soft-focus glow standing in for bloom.
- Re-composing, re-framing, or adding objects not present in the base image.

---
*Generated by Base View Console — pair this file with `brick-facade.jpg` when prompting.*

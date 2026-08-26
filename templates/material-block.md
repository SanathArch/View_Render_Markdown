<!--
  MATERIAL BLOCK — copy one of these into the `materials:` list of a base-view.md
  for every distinct surface zone in the shot (e.g. brick, mortar, steel railing,
  glass, foliage). Keep zones granular: "brick" and "mortar" age differently and
  deserve separate blocks even on the same wall.
-->

- zone: ""                        # e.g. "facade-brick", "window-frame-steel"
  category: ""                    # metal | wood | stone | concrete | fabric | glass | plastic | ceramic | skin | foliage | liquid
  pbr:
    base_color: ""                # hex or named reference
    roughness: ""                 # 0-1, plus description: matte / satin / glossy / mirror
    metallic: ""                  # 0-1, dielectric vs conductor
    specular_or_ior: ""           # e.g. glass 1.5, water 1.33
    normal_detail: ""             # micro-surface description
    height_displacement_mm: ""    # texture relief scale
    subsurface_scattering: ""     # scale + color, if applicable (skin, wax, marble, foliage)
    anisotropy: ""                # brushed-metal / hair / fabric-grain direction, if applicable
    clearcoat: ""                 # car paint / lacquer, if applicable
    opacity_translucency: ""
  texture:
    resolution: ""                # e.g. 4K
    real_world_scale: ""          # texel density, cm/pixel
    tiling: ""
  aging:
    age_category: ""              # pristine | lightly-used | weathered | derelict
    weathering_types:             # list all that apply, each with an intensity
      - type: ""                  # rust | patina | efflorescence | mold-mildew | moss-lichen | grime | uv-fade | cracking | peeling | chipping | scratches | water-staining | graffiti
        intensity_pct: ""         # 0-100
    wear_distribution: ""         # edge-wear / high-contact-points / gravity-streaking / wind-direction / splash-zone
    causal_environment: ""        # coastal-salt / industrial-pollution / desert-uv / humid-tropical / freeze-thaw / urban-grime
    years_of_exposure_implied: ""
  reference_image: ""             # relative path into references/images/materials/

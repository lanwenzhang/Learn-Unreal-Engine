# Lighting

## Project Setting
Dynamic global illumination method: lumen

Use hardware ray tracing when available: on

Shadow map method: virtual shadow map(beta)

## Post Volume
Infinite Extent Unbound: Enable

## Type of Lighting
Directional light: Exterior Sun/Moon light

Sky light

Point light

Spot light

## Lighting mode/method

### Baked lighting/Static lighting
CPU: traditional, cheap, takes a long to bake, light map saved

GPU: through plug-ins, require the RTX card, quick to bake, light map saved

Path tracer: V-RAY, GPU, long time, Architecture

### Dynamic lighting/real-time lighting
RTX: no light map, real-time, quick, expensive, No VR, Low FPS

Lumen lighting: real-time, quick results, no lightmaps, more expensive, VR

## Lightmass importance volume
## Sphere refection capture


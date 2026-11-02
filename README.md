# geoskill-flood-impact-assessment

> Overlay flood extent with population, buildings, roads, and cropland to estimate affected objects and generate impact reports. Use when the user wants to assess flood impact, count affected population/roads/buildings, or generate flood impact summaries from a flood extent raster.

See [SKILL.md](SKILL.md) for full usage, inputs and outputs.

## Quick start

```bash
# Local file mode (backward compatible)
python scripts/flood_impact_assessment.py --flood-raster flood.tif
python scripts/flood_impact_assessment.py --flood-raster flood.tif --population-raster pop.tif
python scripts/flood_impact_assessment.py --flood-raster flood.tif --population-raster pop.tif --roads-file roads.geojson

# Auto-download mode — fetch Sentinel-1 GRD from Microsoft Planetary Computer
# (population raster is synthesized bbox-aware; WorldPop is not on MPC)
python scripts/flood_impact_assessment.py \
    --bbox 116.4,39.6,116.6,39.8 \
    --date-range 2024-06-01,2024-06-30 \
    --output-dir my_output
```

## License

MIT

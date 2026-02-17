# Geothermal Simulator

Interactive browser-based simulator for **Enhanced Geothermal Systems (EGS)** and **Closed-Loop Geothermal** systems.

## Live Demo

**[Launch Simulator →](https://yourusername.github.io/geothermal-simulator/)**

## Features

### Closed-Loop Mode
- Toews & Holmes (2021) analytical solution for lateral heat extraction
- Ramey (1962) wellbore heat transmission for inlet/outlet verticals
- Separate lateral and vertical rock thermal conductivity
- Validated against **Eavor-Lite field data** (MAE ~1-2°C over 16 months)
- Presets: Eavor-Lite (Alberta), Geretsried (Bavaria)

### EGS Mode
- Gringarten et al. (1975) parallel-fracture heat extraction model
- Multi-stage horizontal well with configurable fracture geometry
- Multi-bench, multi-well field layouts
- Far-field heat replenishment after inter-fracture breakthrough
- Presets: Project Cape (Utah), Project Red (Nevada)

### Outputs
- Temperature decline curves (outlet wellhead & lateral/fracture exit)
- Thermal power (MWth) and electric power (MWe) via ORC
- Seasonal ambient temperature effects on ORC efficiency
- Interactive data tables with period-to-period ΔT tracking
- Model Architecture tab with physics documentation
- 3D wellbore visualization

## Deployment

This is a single `index.html` file — no build step required.

### GitHub Pages
1. Create a new repository
2. Upload `index.html`
3. Go to **Settings → Pages → Source: main branch**
4. Your simulator will be live at `https://yourusername.github.io/repo-name/`

### Local
Just open `index.html` in any modern browser.

## Physics

| Component | Method | Reference |
|-----------|--------|-----------|
| Lateral heat extraction (closed-loop) | Quasi-steady radial conduction | Toews & Holmes, GRC 2021 |
| Vertical wellbore heat loss/gain | Ramey's wellbore model | Ramey, JPT 1962 |
| Fracture heat extraction (EGS) | Parallel-fracture conduction | Gringarten et al., JGR 1975 |
| ORC power conversion | Carnot with utilization factor | — |

## Presets

| Preset | Type | Depth | Gradient | Rock Temp | Flow Rate |
|--------|------|-------|----------|-----------|-----------|
| Eavor-Lite | Closed-loop | 2,400m | 31 °C/km | 78°C | 5.76 kg/s |
| Geretsried | Closed-loop | 4,500m | 33.7 °C/km | 160°C | 45 kg/s |
| Project Cape | EGS | 3,960m | 46.5 °C/km | 194°C | 95 kg/s |
| Project Red | EGS | 2,350m | 50 °C/km | 133°C | 63 kg/s |

## Credits

Built with React, Recharts, Three.js, and Tailwind CSS.

Developed by [Enverus Intelligence Research](https://www.enverus.com/) for the *Innovation Underground* podcast.

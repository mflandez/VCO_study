# 1V/Octave VCO - Analog Synthesizer Module

## Project Overview
Analog electronics project designing a voltage-controlled oscillator (VCO) with exponential frequency control for audio synthesis applications. Features 1V/octave response: each 1V increase doubles the output frequency.

## Specifications
- **Inputs:** KEY (0-5V), TUNE (0-1V), LFO (0-1V)
- **Outputs:** Square wave (0-5V), Triangle wave (0-5V)
- **Frequency Range:** ~65 Hz to 2000 Hz (audio spectrum)
- **Supply:** ±5V (Vdd/Vss)

## System Architecture
1. **Input Summer** - Sums KEY, TUNE, LFO control voltages
2. **Exponential Converter** - BJT differential pair for linear-to-exponential conversion
3. **Current-to-Voltage Converter** - Transimpedance amplifier
4. **Oscillator Core** - Integrator + Schmitt trigger with reset transistor

## Key Components
- Op-amps (LM358, TL072 equivalents)
- BJT transistors (matched pair for differential amplifier)
- RC networks for timing
- Output buffers for impedance matching

## Design Features
- Temperature-compensated current source
- Independent square/triangle outputs
- Musical frequency scaling (exponential response)
- PCB designed in KiCad (66×89 mm)

## Performance Notes
- Triangular wave asymmetrical (duty cycle ≠ 50%)
- Requires calibration via TUNE input or trimpots
- Output amplitudes differ (square: 0-5V, triangle: 1.7-3.3V)

## Applications
- Modular synthesizer voice module
- Audio signal generation
- Educational analog design example

## Files
- `ELE8003-VCO-final.pdf` - Complete design documentation
- PCB layouts (KiCad format)

## Authors
Michael Flandez, Arthur Dietrich  
École Polytechnique de Montréal  
ELE8003 - Analog Electronics Projects

## Related Documentation
For full theoretical analysis, circuit simulations, PCB layouts, and implementation details, refer to the complete project report: `ELE8003-VCO-final.pdf`

# Elliptic-iir-filter-design


This project implements the design and analysis of an **elliptic high-pass digital filter** using Python and SciPy. It demonstrates the full workflow from analog filter specification to digital realization, including custom frequency transformation and response visualization.

## Features

- Analog prototype specification and prewarping
- Elliptic filter order estimation
- Analog elliptic prototype design
- Bilinear transform to obtain the digital filter
- Custom low-pass to high-pass frequency transformation
- Magnitude and phase response plotting
- Time-domain visualization of filter output

## Methods Used

- `scipy.special.ellipk`
- `scipy.signal.ellipap`
- `scipy.signal.ellipord`
- `scipy.signal.ellip`
- `scipy.signal.bilinear`
- `scipy.signal.freqs`
- `scipy.signal.freqz`

## Design Parameters

The filter is designed using hard-coded specifications such as:

- Passband edge: `wp = 0.15*pi`
- Stopband edge: `ws = 0.2*pi`
- Passband ripple: `Rp = 1 dB`
- Stopband attenuation: `As = 40 dB`
- Sampling period: `T = 1`
- Sampling frequency: `Fs = 1/T`

A high-pass transformation is also applied using:

- `wphp = 0.2*pi`

## Outputs

The script generates plots for:

- Analog magnitude response
- Analog phase response
- Digital filter magnitude response
- Digital filter phase response
- Elliptic filter response
- Time-domain stem plot

## Purpose

This project is intended as an educational DSP example showing:

- elliptic filter design,
- analog-to-digital filter conversion,
- custom frequency mapping,
- and response analysis.

## Requirements

- Python 3
- NumPy
- SciPy
- Matplotlib

## How to Run
```bash
python proj_az_dsp.py

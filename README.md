# Bachelor Thesis: Michelson Interferometer for Correction of Translation Stage Deviation

LaTeX source of my bachelor thesis in physics, written at the Max Planck Institute of Quantum
Optics (Chair of Laser Physics, LMU Munich), submitted July 2026.

**[Read the PDF](pdf/main_thesis.pdf)**

## Summary

A field-resolved infrared spectroscopy experiment uses a motorized translation stage to set the
optical delay between two laser pulses, so any error in the stage position becomes an error in
the measured signal. This thesis develops an interferometric system to measure the real stage
displacement independently:

- **Laser selection**: characterization of several lasers by wavelength, beam quality (M²) and
  intensity stability
- **Fringe-counting software**: real-time detection with a camera and with photodiodes, and a
  comparison of both
- **Quadrature homodyne interferometer**: two phase-shifted signals that reveal the direction of
  motion, plus a feedback loop that tries to hold the stage at a locked position
- **Integration** into the final experimental setup

Related repositories:
[translation-stage-calibration](https://github.com/carolinakrotschi/translation-stage-calibration)
(measurement software) and
[interferometer-data-analysis](https://github.com/carolinakrotschi/interferometer-data-analysis)
(data and analysis scripts).

## Structure

| Path | Content |
|---|---|
| `main_thesis.tex` | Main document |
| `preamble_thesis.tex` | Packages, macros, title, author and supervisor settings |
| `pages/` | Title pages, abstract, acknowledgements, declarations |
| `chapters/` | Introduction, theory, laser characterization, software, interferometer, integration, conclusion |
| `appendix/` | Appendices, e.g. the list of optical components |
| `figures/` | All figures |
| `sources/` | Bibliography (`biblatex`/`biber`) |
| `WRITING_GUIDE.md` | Cheat sheet for the template's LaTeX macros |

## Build

Requires a TeX distribution with `pdflatex` and `biber`:

```bash
./compile.sh
```

The script compiles into `compilation/` and copies the result to `pdf/main_thesis.pdf`.

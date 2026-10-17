# RippleGL — photonics exploration fork

**A photonics-oriented fork of [Paul Falstad's RippleGL](https://github.com/pfalstad/ripplegl).** The upstream browser ripple-tank simulator supplies the Java/GWT application and WebGL foundation; this fork explores additional media, sources and electromagnetic formulations.

[简体中文](README.zh-CN.md) · [Upstream simulator](https://www.falstad.com/ripple/) · [Source history](docs/README-history.md)

## What differs

Public fork revision `3be54cd` includes photonic-crystal objects, an elliptical photonic-crystal variant, time-varying media, damping/PML experiments, additional examples and changes to the WebGL simulation. The latest historical commit describes a **TE electromagnetic FDTD method under test**; that commit message is not an accuracy benchmark.

On **2026-10-17**, the published fork was **30 commits ahead and 1 behind** upstream `master` (`f8ddee1`). [Fixed-revision comparison](https://github.com/pfalstad/ripplegl/compare/f8ddee15806a27be68f002c0c4bfcf0997029e50...Patr1ck2005:3be54cd5fe54c4f4d0a5c539024f821a004b6a5c) preserves the attribution and actual changed files.

| Source | Contents |
|---|---|
| [src/com/falstad/ripple/client/](src/com/falstad/ripple/client/) | Java/GWT UI and simulation objects |
| `PhotonicCrystal.java`, `PhotonicCrystalEllipse.java` | Fork photonic-crystal objects in that source directory |
| `TimeCrystalMediumBox.java`, `PMLLayer.java` | Experimental time-varying medium and boundary work |
| `war/Ripple.html`, `war/ripple.js` | Web page and WebGL-side code |
| [src/com/falstad/ripple/public/examples/](src/com/falstad/ripple/public/examples/) | Existing example configurations |
| [app/](app/) | Historical Electron wrapper |

## Build and try

The [upstream hosted simulator](https://www.falstad.com/ripple/) demonstrates **upstream RippleGL**, not this fork's additions. No separately verified hosted fork is advertised here.

The original build uses Eclipse for Java with the GWT plugin: import the project, run GWT development mode, or use **GWT Compile Project** to write output into `war/`. Serve the compiled tree and open `Ripple.html`. Full historical instructions remain in the [previous README](docs/README-history.md). The Electron wrapper also requires compiled GWT output; its old Electron dependency is not a current maintained desktop release.

## Scientific and maintenance status

Historical exploration fork. Additional media, damping/PML and electromagnetic code require their own stability, dispersion, boundary-reflection and convergence checks before quantitative scientific use. Existing example names and commit messages do not establish validation. This documentation update did not build the legacy toolchain, run simulations or publish new research results. Separate local rewrites are not part of this public fork's claims.

## License and credits

RippleGL copyright and authorship remain with **Paul Falstad and the upstream contributors**, with GWT port lineage acknowledged to Iain Sharp. The README and source headers specify **GNU GPL version 2 or later**; see the [source header](src/com/falstad/ripple/client/RippleSim.java) and [GNU GPL v2 text](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html). This fork does not replace that license with MIT. Electron and other components retain their own terms.

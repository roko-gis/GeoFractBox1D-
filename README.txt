# GeoFractBox1D

**GeoFractBox1D** is an open-source scientific software package for one-dimensional fractal analysis of geological, geophysical, tectonic, seismological, and other spatial datasets using the classical Box-Counting approach. The software provides a complete workflow for estimating fractal dimensions, evaluating scale dependence, visualizing results, and exporting publication-quality outputs.

GeoFractBox1D has been developed as a research-oriented tool intended for scientists, researchers, graduate students, and professionals working in Earth Sciences and related disciplines. The software emphasizes transparency, reproducibility, and methodological consistency while remaining easy to use through an intuitive graphical interface.

---

# Table of Contents

- Introduction
- Scientific Background
- Methodology
- Features
- Typical Applications
- Software Architecture
- Installation
- Python Dependencies
- Input Data
- Output Files
- Citation
- References
- Licence
---

# Introduction

Many natural geological systems exhibit scale-invariant behavior that cannot be adequately described using classical Euclidean geometry. Fault systems, earthquake hypocenters didtributions, volcanic alignments, mineral occurrences, fractures, geomorphological features, and numerous geological phenomena often display fractal characteristics across multiple spatial scales.

GeoFractBox1D provides an integrated environment for quantitative estimation of fractal dimensions from one-dimensional spatial datasets. It combines established mathematical methodology with modern visualization tools and automated statistical processing.

The software is intended both for exploratory analyses and for production of scientific results suitable for publication.

---

# Scientific Background

Fractal geometry provides one of the most powerful mathematical frameworks for describing complex natural systems exhibiting self-similarity or statistical self-similarity.

Among the numerous techniques for estimating fractal dimensions, the Box-Counting method remains one of the most widely accepted due to its robustness, conceptual simplicity, and applicability to irregular natural datasets.

GeoFractBox1D implements the classical Box-Counting algorithm following the original formulations introduced by:

- Mandelbrot (1982)
- Turcotte (1986)

The implementation follows the theoretical definitions of fractal dimension using logarithmic scaling relationships:

D = - d(log N(ε)) / d(log ε)

where

- D is the fractal dimension
- N(ε) is the number of occupied boxes
- ε is the box size.

The software automatically performs calculations over multiple box sizes, constructs log-log scaling relationships, estimates regression parameters, and evaluates goodness-of-fit statistics.

---

# Methodology

The methodological framework implemented in GeoFractBox1D is based on the classical Box-Counting approach for estimation of one-dimensional fractal dimensions.

The workflow consists of the following stages:

1. Import of one-dimensional spatial data.

2. Automatic normalization and preprocessing of datasets.

3. Generation of logarithmically distributed box sizes.

4. Counting occupied boxes for every spatial scale.

5. Construction of the log(N)-log(ε) relationship.

6. Linear regression within the scaling interval.

7. Estimation of the fractal dimension.

8. Statistical evaluation using:

- coefficient of determination (R²)
- regression residuals
- confidence intervals
- scaling diagnostics

9. Automatic visualization.

10. Export of all numerical and graphical results.

The fractal dimension is estimated using the mathematical formulations described by Mandelbrot (1982) and Turcotte (1986), which remain the international standard for Box-Counting analyses.

Beyond the mathematical implementation, the overall software design and methodological philosophy are strongly inspired by the long-term scientific work of **Prof. Boyko Ranguelov**, whose research has significantly contributed to the application of fractal geometry in geology (including planetary), seismology, tectonics, natural hazards, and Earth system complexity.

GeoFractBox1D translates many of these scientific concepts into a practical computational environment that facilitates reproducible fractal analyses for modern scientific research.

---

# Features

GeoFractBox1D provides a complete environment for one-dimensional fractal analysis including:

• Classical Box-Counting implementation

• Automatic estimation of fractal dimension

• Log-log regression analysis

• Automatic determination of scaling relationships

• Statistical quality assessment

• Calculation of R² values

• Confidence interval estimation

• High-quality scientific plots

• Interactive graphical user interface

• Batch processing of multiple datasets

• Export of figures in publication-quality resolution

• Export of numerical results

• Automatic generation of summary reports

• Reproducible workflows

• Open-source implementation

---

# Typical Applications

GeoFractBox1D is designed primarily for Earth Science applications but can be used for any one-dimensional dataset exhibiting fractal or scale-invariant behavior.

## Scientific Fields

The software has potential applications in:

- Geology
- Structural Geology
- Tectonics
- Geophysics
- Seismology
- Volcanology
- Geomorphology
- Hydrogeology
- Engineering Geology
- Geochemistry
- Environmental Sciences
- Remote Sensing
- Geographic Information Systems (GIS)
- Climate Science
- Physics
- Materials Science
- Ecology
- Complex Systems Research

## Geology and Tectonics

Typical geological applications include:

- Active fault systems
- Fault traces
- Fracture and joint networks
- Lineament analyses
- Structural geology
- Ore deposit distributions
- Mineral occurrences
- Geochemical anomalies
- Geological cross-sections
- Rock discontinuity analyses

## Seismology

The software can be applied to:

- Earthquake hypocenter distributions
- Earthquake epicenter distributions
- Aftershock sequences
- Foreshock–mainshock clustering
- Seismic swarms
- Fault segmentation
- Earthquake migration patterns
- Seismic energy release distributions
- Seismic stations optimisation

## Geomorphology

Applications include:

- River longitudinal profiles
- Drainage networks
- Valley distributions
- Coastal profiles
- Landslide and Rockfalls inventories
- Elevation transects
- Topographic roughness profiles

## Volcanology

Typical datasets include:

- Volcanic vent alignments
- Fissure systems
- Lava flow distributions
- Volcanic fracture systems
- Eruption center distributions

## Hydrogeology

The software can analyze:

- Spring distributions
- Water bodies distributions 
- Well locations
- Aquifer heterogeneity
- Groundwater monitoring profiles
- Fracture-controlled groundwater systems

## Environmental Sciences

Typical applications include:

- Pollution concentration profiles
- Soil contamination surveys
- Environmental monitoring transects
- Ecological spatial distributions
- Environmental hazard assessments
- Waste storage distributions 

## Remote Sensing and GIS

GeoFractBox1D is well suited for spatial datasets extracted from remote sensing and GIS environments, including:

- Lineament extraction from satellite imagery
- Structural lineament mapping
- DEM-derived terrain profiles
- Raster profile analysis
- Surface roughness profiles
- Feature density along profiles
- Edge and fracture extraction products
- Spatial distributions derived from LiDAR datasets
- UAV-derived topographic profiles

## Geophysics

The software can be applied to one-dimensional geophysical datasets such as:

- Gravity anomaly profiles
- Magnetic anomaly profiles
- Electrical resistivity profiles
- Ground Penetrating Radar (GPR) profiles
- Seismic reflection profiles
- Seismic refraction profiles
- Electromagnetic survey profiles
- Borehole measurements records 

## Time-Series Analysis

Although originally developed for one-dimensional spatial datasets, GeoFractBox1D can also be applied to appropriately preprocessed temporal datasets when fractal scaling behavior is investigated.

Potential applications include:

- Earthquake occurrence time series
- Seismic energy release
- Geophysical monitoring records
- Hydrological observations
- Climate records
- Environmental monitoring data
- Laboratory experimental measurements
- Sensor time series
- Continuous monitoring systems

For time-series applications, the data should first be transformed into an appropriate one-dimensional representation suitable for Box-Counting analysis, depending on the scientific objective.

## General Scientific Applications

Beyond Earth Sciences, GeoFractBox1D can also be applied to one-dimensional datasets from numerous scientific disciplines, including:

- Physics
- Planetology
- Astrophysics
- Materials Science
- Biology
- Ecology
- Environmental Monitoring
- Signal Processing
- Image-derived profile analysis
- Network and complexity studies
- Pattern recognition
- Statistical characterization of scale-invariant phenomena

GeoFractBox1D therefore provides a general framework for quantitative one-dimensional fractal analysis wherever fractal organization or scale-invariant behavior is present in observational or experimental datasets.
---

# Software Architecture

GeoFractBox1D is written entirely in Python.

The graphical interface has been designed to provide an intuitive workflow while maintaining complete transparency of the underlying numerical procedures.

The software architecture is modular, allowing future implementation of additional fractal methods, statistical analyses, and visualization capabilities.

Major software components include:

- Graphical User Interface (GUI)
- Data Import Module
- Preprocessing Module
- Box-Counting Engine
- Statistical Analysis Module
- Visualization Module
- Export Module

---

# Installation

GeoFractBox1D is a Python script designed to run inside the **QGIS Python Console**. It does not require standalone installation or integration as a Processing Tool.

## Requirements

- QGIS 3.34 or newer (recommended)
- Python 3.x (included with QGIS)
- Standard Python libraries shipped with QGIS

Depending on future versions, additional Python packages may be required (see the Python Dependencies section).

## Installation in QGIS

### Step 1 – Download the Script

1. Download the latest version of `GeoFractBox1D.py` from the repository.
2. Save the file to a local folder on your computer.

### Step 2 – Open QGIS Python Console

1. Launch QGIS.
2. Open the Python Console:

   **Plugins → Python Console**

3. (Optional) Open the Script Editor for easier execution.

### Step 3 – Run the Script

Run the script directly from the Python Console using:

```python
exec(open(r"C:\path\to\GeoFractBox1D.py").read())---

# Python Dependencies

The software has been developed using Python 3.10+.

Required libraries include:

```
numpy
pandas
matplotlib
scipy
tkinter
Pillow
openpyxl
```

Additional libraries may be included depending on future software extensions.

---

# Input Data

GeoFractBox1D accepts one-dimensional spatial datasets stored in:

- CSV
- TXT
- XLSX

Typical input consists of a single column containing spatial coordinates.

Example:

```
0.42
1.15
2.87
5.42
7.91
...
```

---

# Output Files

The software automatically generates:

- Fractal dimension (D)
- Linear regression parameters
- R² coefficient
- Scaling plots
- Publication-quality figures
- Numerical tables
- Exportable CSV results
- Summary reports

---

# Citation

If you use **GeoFractBox1D** in scientific research, publications, reports, or academic theses, please cite the software appropriately.

The preferred citation is the archived Zenodo release, which provides a permanent DOI and ensures long-term accessibility and reproducibility.

Once the first public release is archived, the citation will be available in this section together with the DOI badge.

### Cite as

> *Citation information will be added upon the first official software release.*

BibTeX, APA, and other citation formats will be available directly from the Zenodo record.

---

# References

## Fundamental Fractal Theory

Mandelbrot, B.B. (1982). *The Fractal Geometry of Nature.* W. H. Freeman and Company, New York.

Turcotte, D.L. (1986). Fractals and fragmentation. *Journal of Geophysical Research*, 91(B2), 1921–1926.

---

## Scientific Inspiration and Methodological Background

The overall methodological philosophy and scientific motivation of GeoFractBox1D are inspired by the long-standing research of **Prof. Boyko Ranguelov**

Representative publications include:

[1] Ranguelov, B., & Dimitrova, S. (2002). Fractal model of the recent surface earth crust fragmentation in Bulgaria. Comptes Rendus de l’Académie Bulgare des Sciences, 55(3).
[2] Ranguelov, B., Dimitrova, S., Gospodinov, D., Spassov, E., Lamykina, G., Papadimitriou, E., & Karakostas, V. (2004). Fractal properties of the South Balkans seismotectonic model for seismic hazard assessment. Proceedings of the 5th International Symposium on Eastern Mediterranean Geology, Thessaloniki.
[3] Ranguelov, B. (2010). Nonlinearities and fractal properties of the European–Mediterranean seismotectonic model. Geodynamics & Tectonophysics, 1(3), 225–230.
[4] Ranguelov, B., & Ivanov, Y. (2017). Fractal properties of the elements of plate tectonics. Journal of Mining and Geological Sciences, Geology and Geophysics, 60(1), 83–89.
[5] Ranguelov, B., Shadiya, F., & Ivanov, Y. (2018). Fractal nature of the Maldives Arc. Proceedings of SGEM 2018, 81–86.

---

# License

GeoFractBox1D is released as open-source software.

The software is intended for scientific research, education, and non-commercial applications.

Users are encouraged to cite the software and the underlying scientific methodology in any publications resulting from its use.

---

# Acknowledgements

GeoFractBox1D has been developed to promote transparent, reproducible, and accessible fractal analysis in Earth Sciences.

The methodological framework is based upon the classical works of Mandelbrot and Turcotte, while the conceptual development and scientific inspiration derive from the extensive research contributions of Prof. Boyko Ranguelov in the fields of fractal geology, seismology, tectonics, and natural hazards.

We gratefully acknowledge these scientific foundations upon which this software has been built.
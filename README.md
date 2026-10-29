# GIC, PSP and corrosion along the Urucu-Manaus gas pipeline

Data and code of the manuscript APPGEO-D-26-01275 (Journal of Applied Geophysics), which models the geomagnetically induced voltages, the pipe-to-soil potential (PSP) and the GIC-related contribution to corrosion along the Urucu-Manaus gas pipeline (GARSOL and GASCOM sections, Amazon region, Brazil) during the geomagnetic disturbances of 21-23 April and 16-17 July 2017.

## Notebooks

| Notebook | What it does | Open in Colab |
|---|---|---|
| `gic_psp_corrosion_workflow.ipynb` | Main workflow: geoelectric field, pipeline discretization, DSTL model, PSP, exposure and corrosion, and the figures of the main text | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LopesMAM/gic-urucu-manaus-pipeline/blob/main/gic_psp_corrosion_workflow.ipynb) |
| `gic_psp_corrosion_supporting_information.ipynb` | Figures S1 to S3 and Tables S4 to S12 of the Supporting Information | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LopesMAM/gic-urucu-manaus-pipeline/blob/main/gic_psp_corrosion_supporting_information.ipynb) |

## How to run

**Google Colab:** open a notebook with the button above and choose *Runtime > Run all*. The first cell downloads this repository.

**Locally:** download the repository, install the packages and run the notebooks inside the repository folder:

```
git clone https://github.com/LopesMAM/gic-urucu-manaus-pipeline.git
cd gic-urucu-manaus-pipeline
pip install numpy pandas geopandas matplotlib jupyter
```

The Supporting Information notebook uses the files saved by the main notebook. If they are not found, it runs the main notebook first. The main notebook takes about 1 minute and the Supporting Information notebook about 1 minute more.

## Data

| Folder | Content |
|---|---|
| `data-magnetometer_MAN/` | One-minute geomagnetic data (declination D and horizontal intensity H) of the Manaus (MAN) magnetometer, one file per day |
| `data-omniweb/` | One-minute IMF Bz, solar wind speed, dynamic pressure and SYM-H from OMNIWeb |
| `data-kp/` | Three-hour Kp index |
| `data-geospatial/basins/` | Shapefile of the Solimões and Amazonas sedimentary basins |
| `data-geospatial/pipeline/` | Shapefile of the GARSOL (Urucu-Coari) and GASCOM (Coari-Manaus) pipelines |

## Outputs

The notebooks create the folder `outputs/` (not stored in the repository):

- `outputs/processed/`: geoelectric field, field parallel to the pipeline, pipeline discretization and circuit parameters, PSP of every node for each terminating impedance, exposure intervals and corrosion per node (CSV files);
- `outputs/figures/`: figures of the main text and of the Supporting Information (PNG files);
- `outputs/tables_si/`: Tables S4 to S12 of the Supporting Information (CSV files).

## License

MIT License (see `LICENSE`).

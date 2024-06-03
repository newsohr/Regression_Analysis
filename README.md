# Regression Analysis with satellite synergy

<!-- ABOUT THE PROJECT -->

## Description of Problem
This programme aims to apply different regression techniques (i.e., Polynomial Regression, Neural Networks, and Gaussian Processes) on sea ice and lead or melt pond classification. The sea ice or melt pond fraction analysis is based on preprocessed colocated Sentinel-2 optical and Sentinel-3 OLCI images.

Melt pond fraction (MPF) is a significant factor affecting the sea ice heat and mass balance, especially during summer (H. Niehaus et al., 2023). It is studied extensively either by retrieving from Sentinel-2 optical data (H. Niehaus et al., 2023) or deriving from Sentinel-3 satellite data (H. Niehaus et al., 2024). Herein, we initialize the analysis by integrating Sentinel-2 and Sentinel-3 data, which hopefully can provide insight for a more accurate interpolation and prediction method on MPF.

Sentinel-3 is a satellite mission launched by the European Space Agency (ESA) in 2016 (Sentinel-3A) and 2018 (Sentinel-3B). It measures the Earth's oceans, land, ice and atmosphere with global coverage. For the ocean particularly, it measures the temperature, colour and height of the sea surface and the thickness of sea ice, which provides extensive information on the sea surface. In this programme, we utilize the data captured by the Ocean and Land Color Instrument (OLCI) optical sensor for analysis.

![S3_OLCI diagram](EO_diagram.png)

The figure (from GEOL0069 week 9 assignment) depicts the OLCI optical sensor layout and Sentinel-3 OLCI basic viewing geometry with the 21 spectral bands, which are used for capturing data across different regions of the electromagnetic spectrum. 5 fan-arranged Camera Optical Sub Assemblies (COSA) are used to detect the 1270km field of views. The assembly is tilted across-track to avoid sun-glint effects. The 21 bands range from 400 to 1020 nm with different spectral and radiometric characteristics. The calibrated products can be processed into gridded images for further usage. Image adapted from Ref [1] and [2].



<!-- GETTING STARTED -->
## Getting Started

The project is built on the notebooks called Colocating_S2_S3_images.ipynb and Regression_analysis.ipynb.

<!-- ### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```
-->
  
## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install essential packages.

For example,

```bash
pip install scikit-image
```


## Usage

<!-- ```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

 USAGE EXAMPLES -->

The notebook starts with an introduction to unsupervised machine learning methods including K-means and Gaussian Mixture Model (GMM). The code of two algorithms is then implemented to classify sea ice and lead based on Sentinel-2 optical data, which produces images similar to the following:

![image](https://github.com/newsohr/GEOL0069/assets/152040156/549021e9-c887-4689-bf53-1b5ac3f8bb32)


The second part is the classification of sea ice and leads based on Sentinel-3 altimetry data. The plots involve the classification of echoes of sea ice and lead from ESA official data and the prediction of GMM. After that, the average of sea ice and lead classification is plotted with the standard deviation filled in.

In the end, a confusion matrix is computed to quantify the classifications of prediction against true values.


<!-- ROADMAP 
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/github_username/repo_name/issues) for a full list of proposed features (and known issues). 
-->



## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.


## License

Distributed under the [MIT](https://choosealicense.com/licenses/mit/) License. 


## Contact

Rhoswen - rhoswen.zeng.20@ucl.ac.uk

Project Link: https://github.com/newsohr/GEOL0069

## Acknowledgments

* []() The input ESA official data is fetched using Google Earth Engine.


## Reference

https://sentiwiki.copernicus.eu/web/s3-mission

Reference:
[1] Craig Donlon, ESA/ESTEC, Mission Science Division, B. Berruti, J. Frerick, C. Mavrocordatos, J. Nieke, H. Rebhan, J. Stroede and the S3 Team. (2008, November 19-20). Sentinel-3 OLCI and SLSTR. Medspiration UCM-6/GlobColour symposium. ESRIN, Frascati, Italy. https://www.globcolour.info/workshop_200811_presentations/3_Future/Donlon-Sentinel-3%20OLCI%20and%20SLSTR-v1.0.pdf
[2] Prikaziuk, E.; van der Tol, C. Global Sensitivity Analysis of the SCOPE Model in Sentinel-3 Bands: Thermal Domain Focus. Remote Sens. 2019, 11, 2424. https://doi.org/10.3390/rs11202424
* []() Quartly GD, Rinne E, Passaro M, Andersen OB, Dinardo S, Fleury S, Guillot A, Hendricks S, Kurekin AA, Müller FL, et al. Retrieving Sea Level and Freeboard in the Arctic: A Review of Current Radar Altimetry Methodologies and Future Perspectives. Remote Sensing. 2019; 11(7):881. https://doi.org/10.3390/rs11070881




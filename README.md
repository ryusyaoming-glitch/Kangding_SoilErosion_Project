This repository contains all files necessary to reproduce the analyses and figures from the PLOS ONE manuscript “Spatiotemporal Characteristics and Driving Factors of Soil Erosion in the Kangding River Basin (Southwest China) Based on the RUSLE Model”. The repository is organized into three main components: Data, Code, and Vectors.
1.Code
Spatiotemporal Characteristics and Driving Factors of Soil Erosion in the Kangding River Basin (Southwest China) Based on the RUSLE Model
Author: Yuqi Guan
This repository contains the code used in the paper:
Spatiotemporal Characteristics and Driving Factors of Soil Erosion in the Kangding River Basin (Southwest China) Based on the RUSLE Model.
We applied CatBoost, XGBoost, and LightGBM to analyze the spatiotemporal variations of soil erosion and its driving factors. SHAP values were used to interpret feature importance across multiple time periods.
DATE：
Input data: CSV file containing Year, driving factors, and target variable (A).
Due to licensing restrictions, raw data are not included here.
Researchers can replace the CSV file path in the script with their own dataset.
How to Run：
(1).Install dependencies:pip install pandas shap matplotlib scikit-learn catboost xgboost lightgbm
(2).Place your dataset (e.g., date.csv) in a local folder.
(3).Update the file path in the script:df = pd.read_csv(r"your_path/40086.csv")
(4).Run the script:python shap_models.py
(5).utput:SHAP summary plots (.png)
SHAP mean values (.xlsx)
Saved under Desktop/shap/[ModelName]/
License：This code is released under the MIT License. You are free to use and modify it with proper citation.
Citation：If you use this code, please cite the following paper:
Yuqi Guan. Spatiotemporal Characteristics and Driving Factors of Soil Erosion in the Kangding River Basin (Southwest China) Based on the RUSLE Model.
2.Data
Sentinel-2 imagery for the study area was downloaded from the Copernicus Open Access Hub (https://scihub.copernicus.eu/) and used for spatial analysis and visualization. precipitation data from the Resource and Environment Data Center, Chinese Academy of Sciences (https://www.resdc.cn, accessed on 25 May 2025); The land use/land cover (LULC) data were obtained from the CNLUCC (China’s Multi-Period Land Use Land Cover Remote Sensing Monitoring Dataset), with a spatial resolution of 30 m (https://www.resdc.cn, accessed on 25 May 2025); Digital elevation model (DEM) data from the Geospatial Data Cloud (https://www.gscloud.cn, accessed on 25 May 2025); and the basic soil erodibility factor data derived from the 1:1,000,000 World Soil Dataset (https://www.ncdc.ac.cn, accessed on 25 May 2025). The normalized difference vegetation index (NDVI) data were obtained from the Resource and Environmental Science Data Platform, with a spatial resolution of 30 m (https://www.resdc.cn, accessed on 25 May 2025). Slope and slope direction data were derived from the DEM. All data used in this study were processed to have a uniform spatial resolution of 30 m.
3.Vectors
This section contains the original vector files used to generate the maps in the manuscript.Includes administrative boundaries for Kangding City and other relevant regionsFile types: Shapefile (.shp, .shx, .dbf, .prj) or GeoJSON.Used in ArcGIS 10.8 to generate figures; files can be projected, clipped, and visualized as needed.All vector data are publicly accessible via the sources listed in the Data section.

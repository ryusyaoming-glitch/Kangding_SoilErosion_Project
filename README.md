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
This section contains the raw datasets used in the study to ensure reproducibility.
Land use data: 30-meter annual land cover dataset from the Resource and Environment Data Center (RESDC)
Soil erodibility factor data: Derived from the 1:1,000,000 World Soil Dataset
Data sources and access links:
Kangding City vector boundary: NGCC (https://www.ngcc.cn, accessed 2025-10-17)
Precipitation: RESDC (https://www.resdc.cn, accessed 2025-10-17)
Land use: RESDC 30-meter annual land cover (https://www.resdc.cn, accessed 2025-10-17)
DEM: Geospatial Data Cloud (https://www.gscloud.cn, accessed 2025-10-17)
Soil factors: 1:1,000,000 World Soil Dataset (https://www.ncdc.ac.cn, accessed 2025-10-17)
Researchers can download these datasets from the public sources above and replace the CSV files in the code.
3.Vectors
This section contains the original vector files used to generate the maps in the manuscript.Includes administrative boundaries for Kangding City and other relevant regionsFile types: Shapefile (.shp, .shx, .dbf, .prj) or GeoJSON.Used in ArcGIS 10.8 to generate figures; files can be projected, clipped, and visualized as needed.All vector data are publicly accessible via the sources listed in the Data section.

# SODIndoorLoc
# **1 Introduction**<br>
&emsp;&emsp;A supplementary open dataset for WiFi indoor localization (**SODIndoorLoc**) was created. It can be treated as a supplement of the UJIIndoorLoc dataset. It covers three buildings and multiple floors within corridors, office rooms and meeting rooms. The total covering area is about 8000 square meters. **1802 points with different locations are arranged**, the number of reference points (RPs) and testing points (TPs) are 1630 and 272, respectively. **23925 samples are recorded, 21205 for training/learning, and 2720 for testing/validation**. The dataset contains 3 kinds of scenes, office room, meeting room, and corridor. Hall and corridor are seamless in these buildings, so there is no distinction between the two scenes. 105 single-band and dual-band APs were pre-installed in the 3 buildings. **Locations of these pre-installed APs and CAD drawings are provided**. Considering differences in the number of samples and MACs in the training data, there are **9 training sheets** and **5 corresponding testing sheets** in the dataset. **The sampling distance** between two adjacent points **is about 1.2 meters in two buildings**, while **the distance is about 0.5 meters in a three-story building**. **The proposed dataset can be used for clustering, classification, and regression** to compare the performance of different indoor positioning applications based on WiFi fingerprint, e.g. high-precision positioning, building, floor or fine-grained scene identification, range model simulation, rapid construction of fingerprint datasets.<br>
# **2 Introduction**<br>
&emsp;&emsp;Jingxue Bi<br>
&emsp;&emsp;bijingxue19@sdjzu.edu.cn<br>
&emsp;&emsp;School of Surveying and Geo-Informatics<br>
&emsp;&emsp;Shandong Jianzhu University<br>
# **3 Cite Request**<br>
Bi, J., Wang, Y., Yu, B. et al. Supplementary open dataset for WiFi indoor localization based on received signal strength. Satell Navig 3, 25 (2022). https://doi.org/10.1186/s43020-022-00086-y<br>
# **4 Files**<br>
&emsp;&emsp;There are 4 folders in the './SODIndoorLoc/' path, where 3 folders denote 3 buildings, CETC331, HCXY, SYL, the other folder stores relavant figures. In addition, an Excel document and a CAD document within 3 buildings are provided in the './SODIndoorLoc/' path.<br>
## **(1)Two csv files are in the CETC331 folder**<br>
&emsp;&emsp;<font color="red">_Training_CETC331.csv_</font>: Data used for training models in the CETC331 building. The following figure is a fragment of the Training_CETC331.csv file.<br>
![image](https://github.com/renwudao24/SODIndoorLoc/blob/main/images/Training_CETC331.png)
&emsp;&emsp;<font color="red">_Testing_CETC331.csv_</font>:Data used to test models in the CETC331 building. At each TP, 10 samples are stored in the sheet.<br>
## **(2) Six csv files are in the HCXY folder**<br>
&emsp;&emsp;<font color="Blue">_Training_HCXY_All_30.csv_</font>: Data used for training models in the HCXY building with all detected MACs. At each RP, there are 30 samples stored in the sheet.<br>
&emsp;&emsp;<font color="Blue">_Training_HCXY_AP_30.csv_</font>: Data used for training models in the HCXY building with MACs of pre-installed APs. At each RP, there are 30 samples stored in the sheet.<br>
&emsp;&emsp;<font color=Blue>_Training_HCXY_All_Avg.csv_</font>: Data used for training models in the HCXY building with all detected MACs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.<br>
&emsp;&emsp;<font color=Blue>_Training_HCXY_AP_Avg.csv_</font>: Data used for training models in the HCXY building with MACs of pre-installed APs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.<br>
&emsp;&emsp;<font color=Blue>_Testing_HCXY_All.csv_</font>:Data used to test models in the HCXY building with all detected MACs. At each TP, 10 samples are stored in the sheet.<br>
&emsp;&emsp;<font color=Blue>_Testing_HCXY_AP.csv_</font>:Data used to test models in the HCXY building with all MACs of pre-installed APs. At each TP, 10 samples are stored in the sheet.<br>
## **(3) Six csv files are in the SYL folder**<br>
&emsp;&emsp;<font color=Blue>_Training_SYL_All_30.csv_</font>: Data used for training models in the SYL building with all detected MACs. At each RP, there are 30 samples stored in the sheet.<br>
&emsp;&emsp;<font color=Blue>_Training_SYL_AP_30.csv_</font>: Data used for training models in the SYL building with MACs of pre-installed APs. At each RP, there are 30 samples stored in the sheet.<br>
&emsp;&emsp;<font color=Blue>_Training_SYL_All_Avg.csv_</font>: Data used for training models in the SYL building with all detected MACs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.<br>
&emsp;&emsp;<font color=Blue>_Training_SYL_AP_Avg.csv_</font>: Data used for training models in the SYL building with MACs of pre-installed APs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.<br>
&emsp;&emsp;<font color=Blue>_Testing_SYL_All.csv_</font>:Data used to test models in the SYL building with all detected MACs. At each TP, 10 samples are stored in the sheet.<br>
&emsp;&emsp;<font color=Blue>_Testing_SYL_AP.csv_</font>:Data used to test models in the SYL building with all MACs of pre-installed APs. At each TP, 10 samples are stored in the sheet.<br>
## **(4) The xlsx file**<br>
&emsp;&emsp;_Information of pre-installed APs.xlsx_: In this xlsx file, there are 3 sheets. They are named as CETC331, HCXY, and SYL in order, 26 dual-band APs for CETC331, 56 single-band APs for HCXY, and 23 dual-band APs for SYL. Locations of APs, the numbered MAC addresses, frequency in MHz can be found in the xlsx file. The following figure is an example of information of pre-installed APs in the SYL building.<br>
![image](https://github.com/renwudao24/SODIndoorLoc/blob/main/images/Information%20of%20pre-installed%20APs.png)
# **5 Attribute Information**<br>
&emsp;&emsp;Buildings are in different cities, MACs in different buildings are distinct. Suppose tha the number of MACs in a building is n.<br>
&emsp;&emsp; <font color=Blue>_Attribute value 001 (**MAC001**)_</font>: RSS value for MAC001. Negative integer values from -104 to 0 and +100. Positive value 100 used if MAC001 was not detected.<br>
…<br>
&emsp;&emsp;<font color=Blue>_Attribute value n (**MACn**)_</font>: RSS value for MAC00n. Negative integer values from -104 to 0 and +100. Positive value 100 used if MAC001 was not detected.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+1 (**ECoord**)_</font>: East coordinate in meters in the local coordinate system.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+2 (**NCoord**)_</font>: North coordinate in meters in the local coordinate system.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+3 (**FloorID**)_</font>: Floor level from 1 to 3 and 4.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+4 (**BuildingID**)_</font>: Range from 1 to 3, corresponding to CETC331, HCXY and SYL in sequence.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+5 (**SceneID**)_</font>: Range from 1 to 3, corresponding to corridor, office room and meeting room in sequence.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+6 (**UserID**)_</font>: Range from 1 to 10, who participate WiFi collection.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+7 (**PhoneID**)_</font>: Range from 1 to 9, which smartphone was used for WiFi collection.<br>
&emsp;&emsp;<font color=Blue>_Attribute value n+8 (**SampleTimes**)_</font>: Range from 1 to 30, recording the count of samples.<br>
&emsp;&emsp;The detailed information can be found in the **Description of the SODIndoorLoc dataset**.<br>

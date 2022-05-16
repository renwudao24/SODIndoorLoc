# SODIndoorLoc
**1 Introduction**
&emsp;&emsp;A supplementary open dataset for WiFi indoor localization (**SODIndoorLoc**) was created. It can be treated as a supplement of the UJIIndoorLoc dataset. It covers three buildings and multiple floors within corridors, office rooms and meeting rooms. The total covering area is about 8000 square meters. **1802 points with different locations are arranged**, the number of reference points (RPs) and testing points (TPs) are 1630 and 272, respectively. **23925 samples are recorded, 21205 for training/learning, and 2720 for testing/validation**. The dataset contains 3 kinds of scenes, office room, meeting room, and corridor. Hall and corridor are seamless in these buildings, so there is no distinction between the two scenes. 105 single-band and dual-band APs were pre-installed in the 3 buildings. **Locations of these pre-installed APs and CAD drawings are provided**. Considering differences in the number of samples and MACs in the training data, there are **9 training sheets** and **5 corresponding testing sheets** in the dataset. **The sampling distance** between two adjacent points **is about 1.2 meters in two buildings**, while **the distance is about 0.5 meters in a three-story building**. **The proposed dataset can be used for clustering, classification, and regression** to compare the performance of different indoor positioning applications based on WiFi fingerprint, e.g. high-precision positioning, building, floor or fine-grained scene identification, range model simulation, rapid construction of fingerprint datasets.
**2 Introduction**
&emsp;&emsp;Jingxue Bi
&emsp;&emsp;bijingxue19@sdjzu.edu.cn
&emsp;&emsp;School of Surveying and Geo-Informatics
&emsp;&emsp;Shandong Jianzhu University
**3 Cite Request**
&emsp;&emsp;Jingxue Bi. Supplementary Open Dataset for WiFi Fingerprint-based Indoor Localization. https://github.com/renwudao24/SODIndoorLoc.
**4 Files**
&emsp;&emsp;Three folders denote 3 buildings, CETC331, HCXY, and SYL.
**(1)Two csv files are in the CETC331 folder**
&emsp;&emsp;<font color=Blue>Training_CETC331.csv</font>: Data used for training models in the CETC331 building.
&emsp;&emsp;<font color=Blue>Testing_CETC331.csv</font>:Data used to test models in the CETC331 building. At each TP, 10 samples are stored in the sheet.
**(2) Six csv files are in the HCXY folder**
&emsp;&emsp;<font color=Blue>Training_HCXY_All_30.csv</font>: Data used for training models in the HCXY building with all detected MACs. At each RP, there are 30 samples stored in the sheet.
&emsp;&emsp;<font color=Blue>Training_HCXY_AP_30.csv</font>: Data used for training models in the HCXY building with MACs of pre-installed APs. At each RP, there are 30 samples stored in the sheet.
&emsp;&emsp;<font color=Blue>Training_HCXY_All_Avg.csv</font>: Data used for training models in the HCXY building with all detected MACs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.
&emsp;&emsp;<font color=Blue>Training_HCXY_AP_Avg.csv</font>: Data used for training models in the HCXY building with MACs of pre-installed APs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.
&emsp;&emsp;<font color=Blue>Testing_HCXY_All.csv</font>:Data used to test models in the HCXY building with all detected MACs. At each TP, 10 samples are stored in the sheet.
&emsp;&emsp;<font color=Blue>Testing_HCXY_AP.csv</font>:Data used to test models in the HCXY building with all MACs of pre-installed APs. At each TP, 10 samples are stored in the sheet.
**(3) Six csv files are in the SYL folder**
&emsp;&emsp;<font color=Blue>Training_SYL_All_30.csv</font>: Data used for training models in the SYL building with all detected MACs. At each RP, there are 30 samples stored in the sheet.
&emsp;&emsp;<font color=Blue>Training_SYL_AP_30.csv</font>: Data used for training models in the SYL building with MACs of pre-installed APs. At each RP, there are 30 samples stored in the sheet.
&emsp;&emsp;<font color=Blue>Training_SYL_All_Avg.csv</font>: Data used for training models in the SYL building with all detected MACs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.
&emsp;&emsp;<font color=Blue>Training_SYL_AP_Avg.csv</font>: Data used for training models in the SYL building with MACs of pre-installed APs. At each RP, there is only 1 sample stored in the sheet. The sample is the average of 30 samples.
&emsp;&emsp;<font color=Blue>Testing_SYL_All.csv</font>:Data used to test models in the SYL building with all detected MACs. At each TP, 10 samples are stored in the sheet.
&emsp;&emsp;<font color=Blue>Testing_SYL_AP.csv</font>:Data used to test models in the SYL building with all MACs of pre-installed APs. At each TP, 10 samples are stored in the sheet.
**5 Attribute Information**
&emsp;&emsp;Buildings are in different cities, MACs in different buildings are distinct. Suppose tha the number of MACs in a building is n.
&emsp;&emsp;<font color=Blue>Attribute value 001 (**MAC001**)</font>: RSS value for MAC001. Negative integer values from -104 to 0 and +100. Positive value 100 used if MAC001 was not detected.
…
&emsp;&emsp;<font color=Blue>Attribute value n (**MACn**)</font>: RSS value for MAC00n. Negative integer values from -104 to 0 and +100. Positive value 100 used if MAC001 was not detected.
&emsp;&emsp;<font color=Blue>Attribute value n+1 (**ECoord**)</font>: East coordinate in meters in the local coordinate system.
&emsp;&emsp;<font color=Blue>Attribute value n+2 (**NCoord**)</font>: North coordinate in meters in the local coordinate system.
&emsp;&emsp;<font color=Blue>Attribute value n+3 (**FloorID**)</font>: Floor level from 1 to 3 and 4.
&emsp;&emsp;<font color=Blue>Attribute value n+4 (**BuildingID**)</font>: Range from 1 to 3, corresponding to CETC331, HCXY and SYL in sequence.
&emsp;&emsp;<font color=Blue>Attribute value n+5 (**SceneID**)</font>: Range from 1 to 3, corresponding to corridor, office room and meeting room in sequence.
&emsp;&emsp;<font color=Blue>Attribute value n+6 (**UserID**)</font>: Range from 1 to 10, who participate WiFi collection.
&emsp;&emsp;<font color=Blue>Attribute value n+7 (**PhoneID**)</font>: Range from 1 to 9, which smartphone was used for WiFi collection.
&emsp;&emsp;<font color=Blue>Attribute value n+8 (**SampleTimes**)</font>: Range from 1 to 30, recording the count of samples.
&emsp;&emsp;The detailed information can be found in the **Description of the SODIndoorLoc dataset**.

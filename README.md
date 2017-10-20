Brief description for files in this directory
Witten by Dr. Hisashi SATO (JAMSTEC) on 20 Oct 2017

This folder contains data files those are emplyed by the anaysis in the Sato and Kobayashi (2017) JGR-Biogeosciences. Some output files of the analysis are also available in this floder. For detailed descriptions about the natures of the data, please refer the Sato & Kobayashi (2017) JGR-Biogeosciences.

Every geographical data-sets are trimmed into the rectangular externt of N45-75 W80-170. All data for inputing the analysis were higher-level products those are made from original data, all of which have their own copywrights.

_____________________________________________
A. Preparation

Some large files are splited into piece files, because only files less than 25MB can be uploaded on the github. Please combine piece files together with the following command on linux.
	cat LAI_YearMean* > LAI_YearMean.dat
	cat giems_d15_V10_* > giem_d15_V10.csv
	cat ASTER-GDEM-Siberia-DEM* > ASTER-GDEM-Siberia-DEM.dat
	cat ASTER-GDEM-Siberia-NSindex* > ASTER-GDEM-Siberia-NSindex.dat
	cat ASTER-GDEM-Siberia-Slope* > ASTER-GDEM-Siberia-Slope.dat

_____________________________________________
B. Geographical distributions of environmental variablese thoses are emplyed by the Principal Component Analysis (PCA)

File name:	ASTER-GDEM-Siberia-DEM.dat
Description:	Elevation @ 1/112 degree
File type:	2 byte integer without sign
Unit:		m

File name:	ASTER-GDEM-Siberia-Slope.dat
Description:	Slopeness @ 1/112 degree
File type:	2 byte integer without sign
Unit:		degree

File name:	ASTER-GDEM-Siberia-NSindex.dat
Description:	Aspect @ 1/112 degree
File type:	2 byte integer without sign
Unit:		degree * 10000.0

File name:	Average_SoilDepth.csv
Description:	Soil Depth @ 0.5 degree
Unit:		m
Code for missing value:	-999.0

File name:	giems_d15_v10-45-75N-80-170.csv
Description:	Innundation record @1/112 degree, converted from GIEMS
Code for water surface:				-1.0
Code for land without inundation record:	0.0
Code for land with inundation record:		1.0

File name:	CAMPGIV2-permafrost-45-75N-80-170.csv
Description:	Permafrost coverage @ 0.5 degree
Unit:		Percent
Code for missing value:	-999.0
- Correspondence table of values here to code in the original data -
	Value	Original Code
	0%	Land witout permafrost   
	5%	Isolated patches ( 0- 10%) & Relict permafrost
	30%	Sporadic         (10- 50%) permafrost
	70%	Discontinuous    (50- 90%) permafrost
	95%	Continuous       (90-100%) permafrost

File name:	Latitude.csv
Description:	Latitude of the center location of 0.5 degree grid cell
		Only one value is available for each latitudinal band

File name:	Average_CRU_Precip.csv
Description:	Average Annual Precipitation @ 0.5 degree
Unit:		mm/year
Code for missing value:	-999.0

File name:	Average_CRU_GDD5.csv
Description:	Average GDD5 @ 0.5 degree
Unit:		Celsius * day
Code for missing value:	-999.0


_____________________________________________
C. Geographical distributions of larch LAI, which is emplyed by the Multiple Regression Analysis

File name:	LAI_YearMean.dat
Description:	Larch LAI @ 1/112 degree grid
File type:	4 byte real number
Unit:		m2/m2
Code for Water body:	100.0
Code for Larch, but not estimated by the noise:	200.0
Code for Non-Larch:	300.0


_____________________________________________
D. Factor loadings of the principal components 1, 2, and 3 of the PCA.

File name:	FactorLoadings.csv
Description:	This data is consistent with the Figure 2 in the Sato & Kobayashi (2017).


_____________________________________________
E. 0.5 degree-grid averages of Principal Component 1 and 2

File name:	out_PC1.csv
File name:	out_PC2.csv
Description:	This data is consistent with the Figure 3a and 3b in the Sato & Kobayashi (2017).

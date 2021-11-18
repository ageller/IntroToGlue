# Data Sets

Please see the jupyter notebook ([PrepChicagoData.ipynb](https://github.com/ageller/IntroToGlue/blob/main/data/PrepChicagoData.ipynb)) in this repository for more details.  In general, I downloaded data from the following websites and then took only the columns I was interested in (and converted some to numerical values) for the files in the repo.  Hopefully the column names self explanatory.

Data were downloaded from the  [Chicago Data Portal](https://data.cityofchicago.org/).
- Crimes
  - Original dataset: Public-Safety / [Crimes-2001-to-Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/data) (2021 data)
  - [ChicagoCrime_10k.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoCrime_10k.csv) (first 10k lines)
  - [ChicagoCrime.csv](https://drive.google.com/file/d/1Kx7Kr-hj7Nb6LatpG4zC-o2XiEARHPqC/view?usp=sharing) (full file, 175k lines, on Google Drive )
- Taxis
  - Original dataset: Transportation / [Taxi Trips](https://data.cityofchicago.org/Transportation/Taxi-Trips/wrvz-psew/data) (2021 data)
  - [ChicagoTaxi_10k.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoTaxi_10k.csv) (first 10k lines)
  - [ChicagoTaxi.csv](https://drive.google.com/file/d/1QfXInoBSQOYY7OtkqcaWms9OROCW6T_t/view?usp=sharing) (full file, 3.1M lines, on Google Drive)
  - [ChicagoTaxiMeans.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoTaxiMeans.csv) (Mean values at each pickup location)
- Building Permits
  - Original dataset: Buildings / [Building-Permits](https://data.cityofchicago.org/Buildings/Building-Permits/ydr8-5enu/data) (2021 data with latitude and longitude)
  - [ChicagoPermits_10k.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoPermits_10k.csv) (first 10k lines)
  - [ChicagoPermits.csv](https://drive.google.com/file/d/1P7M8yYfFEOl9OV-MmZKL1M_P6FMRPYj8/view?usp=sharing) (full file 36k lines, on Google Drive)
- Affordable Housing
  - Original dataset: Community-Economic-Development / [Affordable-Rental-Housing-Developments](https://data.cityofchicago.org/Community-Economic-Development/Affordable-Rental-Housing-Developments/s6ha-ppgi/data)
  - [ChicagoHousing.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoHousing.csv)
- Public Schools
  - Original dataset: Education / [Chicago-Public-Schools-School-Progress-Reports-SY2](https://data.cityofchicago.org/Education/Chicago-Public-Schools-School-Progress-Reports-SY2/ngix-dc87/data)
  - [ChicagoSchools.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoSchools.csv)
- COVID-19 Vaccinations
  - Original dataset: Health-Human-Services / [COVID-19-Vaccinations-by-ZIP-Code](https://data.cityofchicago.org/Health-Human-Services/COVID-19-Vaccinations-by-ZIP-Code/553k-3xzc/data)
  - [ChicagoVaccine.csv](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoVaccine.csv)
- Chicago map
   - Satellite map of Chicago was downloaded using Google's Earth Engine.  See details in the [PrepChicagoData.ipynb](https://github.com/ageller/IntroToGlue/blob/main/data/PrepChicagoData.ipynb) notebook.
   - Street shapfile to test : Facilities & Geographic Boundaries / [Street Center Lines](https://data.cityofchicago.org/Transportation/Street-Center-Lines/6imu-meau)
   - [ChicagoGeoTIFF.tif](https://github.com/ageller/IntroToGlue/blob/main/data/ChicagoGeoTIFF.tif)
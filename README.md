# Indonesia_Covid19_With_Folium
Data Visualisation Covid19 in Indonesia On Map 

# Don't forget to set your working directory in Colab
cd /content/gdrive/MyDrive/GIS #is my working directory

# You can used excel file to process the data if connection to url json file is invalid

import glob\
#Membaca semua data kemudian menggabungkannya menjadi satu\
Data_Covid = pd.DataFrame(columns=['tanggal', 'KASUS', 'MENINGGAL', 'SEMBUH', 'DIRAWAT_OR_ISOLASI',
       'AKUMULASI_KASUS', 'AKUMULASI_SEMBUH', 'AKUMULASI_MENINGGAL',
       'AKUMULASI_DIRAWAT_OR_ISOLASI','Propinsi'])\
       
files = glob.glob(r'DataCovid*.xlsx')\
for f in files:\
&nbsp;&nbsp;&nbsp;&nbsp;print(f)\
&nbsp;&nbsp;&nbsp;&nbsp;Data = pd.read_excel(f'{f}')\
&nbsp;&nbsp;&nbsp;&nbsp;Data_Covid = pd.concat([Data,Data_Covid])\
&nbsp;&nbsp;&nbsp;&nbsp;print(Data_Covid.shape)

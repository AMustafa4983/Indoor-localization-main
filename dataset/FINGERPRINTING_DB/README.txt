Copyright (c) 2017, Tampere University of Technology (TUT)
These data is licensed under CC Attribution 4.0 International (CC BY).
This documentation is licensed under CC0 license.


This folder contains the WLAN RSS fingerprint data described in <ref to paper,
e.g. Lohan et al. 2017> and provided at <unique link to data>.

This folder contains the following 8 csv-files with the measurement data. The
data is of two types: 

1) training data (15% of the whole data)
 Test_coordinates_21Aug17.csv
 Test_date_21Aug17.csv
 Test_device_21Aug17.csv
 Test_rss_21Aug17.csv

2) test data (85% of the whole data):
 Training_coordinates_21Aug17.csv
 Training_date_21Aug17.csv
 Training_device_21Aug17.csv
 Training_rss_21Aug17.csv


Each of these data types is described by 4 csv-files as follows:

   a) Coordinates file: each row shows the (x,y,z) coordinate (in meters) where the
      measurement were done. These are the local coordinates, not the GPS coordinates, so
      that they can be directly used for positioning studies. Example:
      $(x,y,z)=(137.24,19.731,0)$ for the first measurement in the test fingerprints.

   b) RSS file: this is a large file with N_AP columns, showing the RSS level at which 
      each of the N_AP MAC addresses were heard in each measurement point. Each row 
      corresponds to one measurement.  The non-heard APs are set to +100 dB, which is 
      a fixed bogus value. If a MAC address is heard, then it is heard at a negative 
      level (in dB). For example, in the training RSS file, the access point 2 was 
      not heard (i.e. value 100), the access point 420 was heard at -84 dB, and the 
      access point 489 was heard with -52 dB.

   c) Date file: this is a single column file, where each row shows the date at which 
      each measurement from the corresponding training or test sets was done. 
      For example, the  measurement indexed 1 from the Test data was taken on 18.8.2017
      at time 11:59:23. The measurement dates are not sorted chronologically; they were 
      parsed in a non-chronological order on the cloud server where the measurements 
      were done. However the four training data files are perfectly synchronized, meaning 
      that the n-th row in each of the training file is always matched to the n-th row 
      in the other training files, with n=1,...,697. Similarly, the four test data 
      files are also synchronized.

   d) Device file: this is another single column file, where each row shows what Android 
      device was used for that particular measurement. For example, the 3rd measurement 
      in the training data was collected with a Samsung SM-A10F device and the 15th 
      measurement in the test data was collected with a Xiaomi MI MAX 2 device.


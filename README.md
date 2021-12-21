# AF2align

The program align output pdb file and extract pae plddt values to [.csv] for Alphafold 2.1.1

# Install

$ cd /path/to/storage/

$ git clone https://github.com/CYP152N1/AF2align

This program was perfomend just by python3. 

Modules (os, sys, pickle, csv, sys, time, numpy, argparse, math) were requred in python3 packeges.


# How to Use

$ cd /path/to/output/of/Alphafold2.1.1

$ python /path/to/storage/plddt2csv/align_mono.py

$ python /path/to/storage/plddt2csv/align_ptm.py

$ python /path/to/storage/plddt2csv/align_multi.py


If you align chain B at the three residues (20, 55, 80)

$ python /path/to/storage/plddt2csv/align_multi.py -alc 2 -al1 20 -al2 55 -al3 80

additional arguments were shown below.


# Optional Argument
'-i', default='result_model',   help='input XXXXX if [XXXXX_Y_ptm.pkl]

'-m', default='relaxed_model',  help='input ZZZZZ if [ZZZZZ_Y_ptm.pdb]

'-n', default='5',              help='input Y if you want open [XXXXX_1_ptm.pkl,XXXXX_2_ptm.pkl ... ,XXXXX_5_ptm.pkl]

'-d', default='',               help='ignored residue number for average pLDDTs caliculation to determined the ranking of models [1-5_56-75_105-135]; 
                                      !!this argument is not suport for chain number!!.
                                      

'-alc', default="1",            help='Change chain number from first chain to other chain

'-al1', default=0,              help='Center the mid point of al1 and al3, the point (al1) shift on x-axis'; if -al1 = 0, 1/4 of residue number was used for alignment

'-al2', default=0,              help='The point (al3) shift on xy-plane'; 3/4 of residue number was used for alignment'; 2/4 of residue number was used for alignment

'-al3', default=0,              help='Center the mid point of al1 and al3, the point (al3) shift on x-asis and opozit site of al1'

# Alignment Examples

![image](https://user-images.githubusercontent.com/87903303/146930576-c7e6c776-833e-421a-8a42-b8f64f9cdfef.png)

# Logs
![image](https://user-images.githubusercontent.com/87903303/146928560-18d1f41e-a519-45b0-8e2e-db96c521665d.png)

![image](https://user-images.githubusercontent.com/87903303/146928607-3b59b8cf-4f2a-4f87-b3f7-2e7cf72c0ef0.png)

![image](https://user-images.githubusercontent.com/87903303/146928650-826f2ec2-e96a-43d2-adb1-70c8f702d0ad.png)

# Output

??_plddt.csv

![image](https://user-images.githubusercontent.com/87903303/146928814-b3e4fb53-1af5-40dd-8ddc-5d147a5f9bad.png)


??_pae_m?_???.csv

![image](https://user-images.githubusercontent.com/87903303/146930311-4ae03f9b-d15b-4797-8473-afafbb7c9eea.png)



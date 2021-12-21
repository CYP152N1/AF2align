# AF2align

The program align output pdb file and extract pae plddt values to [.csv] for Alphafold 2.1.1

# Install

$ cd /path/to/storage/

$ git clone https://github.com/CYP152N1/AF2align

This program was perfomend just by python3. 
modules (os, sys, pickle, csv, sys, time, numpy, argparse, math) were requred in python3 packeges.

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



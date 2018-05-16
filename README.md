For the full codes, please ask to repo's owner
Dependencies:
  
  * python 3.6
  * pip3
  * anaconda3
  * libstdc++.so.6.0.24
  * matplotlib
  * sklearn
  * scipy

Installation Modules:
pip3 install matplotlib
pip3 install sklearn
pip3 install scipy

Issue:
  * CXXABI_1.3.9 not included in libstdc++.so.6

solved:
    
    Confirm that there is an libstdc++.so.6.0.24 in ~/anaconda3/lib/:
    $ ls libstdc++.so.6.0.24
    
    Confirm that there is a symlink libstdc++.so.6 in ~/anaconda3/lib/:
    $ ls libstdc++.so.6
    
    Remove the existing symlink (in my case libstdc++.so.6 -> libstdc++.so.6.0.19):
    $ rm ~/anaconda3/lib/libstdc++.so.6
    
    Relink it to libstdc++.so.6.0.24:
    $ ln -s /home/arissetyawan/anaconda3/lib/libstdc++.so.6.0.24 /home/arissetyawan/anaconda3/lib/libstdc++.so.6

Run Test

/home/arissetyawan/anaconda3/bin/python3.6 task_dna.py

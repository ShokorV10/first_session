# speech processing first session materials
These are the materials you will need for the first practical session of speech processing. please follow the instructions to install the requirements localy and contact [me](mouhamadaboshokor@gmail.com) if you have any issues I would mostly be able to respond in the evening 

**Please Note that using a Linux distribution like ubuntu or an emulator through VMs is highly advisable and will save a ton of work throughout this tutorial I assume that you have a debian installed or an emulator**

### install the python requirements in a separate venv
~~~
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
~~~
 
### install festival and test it
* install main packages   
~~~
sudo apt-get install festival festlex-cmu festlex-poslex festlex-oald libestools1.2 unzip festvox-don
~~~
* test festival this command should open festival prompt
~~~
festival
~~~
* download the CMU_arctic voices (Note this might take some time depending on your internet)
~~~
mkdir cmu_tmp
cd cmu_tmp/
wget -c http://www.speech.cs.cmu.edu/cmu_arctic/packed/cmu_us_awb_arctic-0.90-release.tar.bz2
~~~
* extract them and move them to festival 
~~~
for d in `ls /usr/share/festival/voices/english` ; do
if [[ "$d" =~ "cmu_us_" ]] ; then
sudo mv "/usr/share/festival/voices/english/${d}" "/usr/share/festival/voices/english/${d}_clunits" 
fi ; done
~~~  



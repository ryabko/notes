Python settings in MacOS:
~/Library/Application\ Support/pip/pip.conf

Create a virtual environment.
You may need to run `sudo apt-get install python3-venv` first
```
python3 -m venv .venv
```
Save installed packages into the file
```
pip3 freeze > requirements.txt
```
Install packages from the file
```
pip3 install -r requirements.txt
```

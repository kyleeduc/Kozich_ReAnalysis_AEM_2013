#README

Obtained the Linux version of mothur (v1.48.3) from the mothur GitHub repository

```bash
wget --no-check-certificate https://github.com/mothur/mothur/releases/download/v1.48.3/Mothur.linux_8.zip
mkdir -p code
unzip Mothur.linux_8.zip
mv Mothur.linux_8/mothur code/
rm Mothur.linux_8.zip
rm -rf __MACOSX
```
My version of ubuntu does not work well with the "Mothur.linux_8.zip" file, so I followed a procedure to compile mothur from source:

1. Mother needs compilers, CMake, and libraries
```bash
sudo apt-get update
sudo apt-get install -y build-essential cmake git g++ make \
    zlib1g-dev libncurses5-dev
```
2. Download the source code
```bash
wget --no-check-certificate https://github.com/mothur/mothur/archive/refs/tags/v1.48.3.tar.gz
tar -xvzf v1.48.3.tar.gz
mv mothur-1.48.3 mothur_source
```
3. Build mothur
```bash
cd mothur_source
make -j4
```
4. Move the compiled binary
```bash
mkdir -p ~/code
mv mothur ~/code/
```

mothur should output the version by doing...

```bash
~/code/mothur -v
```








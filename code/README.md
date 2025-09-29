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

mothur should output the version by doing...

```bash
~/code/mothur -v
```







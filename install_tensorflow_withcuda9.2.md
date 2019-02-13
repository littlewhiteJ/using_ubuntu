# how to install tensorflow (especially with cuda 9.2)

## not using a GPU
first, if you do not have a super GPU, it is easy to type
```
  pip install tensorflow
```
to install a CPU version

## but if you want to install a GPU version easily, such as 
```
  pip install tensorflow-gpu
```
, it is not recommended using the newest cuda9.2. there are errors here.

so here are the tips:
### using cuda 9.0
it is easy to find an old version on Nvidia

### using conda
first download anaconda

here you should be clear that the newest version of anaconda may be not easy to use, as the newest anaconda using python 3.7...

so you may choose another older one [here](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/)

then install anaconda by 
```
  bash Anaconda----blabla----.sh
```
if you are in China, it is recommended to use source in USTC
```
  conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
  conda config --add channels https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
  conda config --set show_channel_urls yes
``` 
  
after install it, you can install tensorflow by 
```
  conda install -c anaconda tensorflow-gpu
``` 
### using source code by Google

it is easy to found on stackoverflow...

so i skipped.

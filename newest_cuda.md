## we install a Nvidia driver, a cuda, a cudnn and a pytorch here

[here](https://zhuanlan.zhihu.com/p/35532314) is the newest installing methods for CUDA and CUDNN and pytorch

but not in detail and

no error!!!

actually i meet so many errors here

### install Nvidia drivers

- disable nouveau
before install the latest Nvidia drivers, you should disable this... and reboot

then your display will be so ugly that you just want to install Nvidia drivers as quick as possible

[here](https://askubuntu.com/questions/841876/how-to-disable-nouveau-kernel-driver) is the method to disable nouveau

### install cuda

- missing library
when you install cuda you may encounter that mistake

and [here](https://stackoverflow.com/questions/22360771/missing-recommended-library-libglu-so) is the solution


- compiler mistake 
you may meet **unsupported compiler: 7.3.0 cuda**

just use --override

so the end is

```
sudo sh cuda_9.1.85_387.26_linux.run --toolkit --toolkitpath=/usr/local/cuda-9.1 -no-opengl-libs --silent --override
```

and do not forget the environment setting 

it helps [here](https://zhuanlan.zhihu.com/p/35509593)

### install cudnn
more easy here

[it](https://zhuanlan.zhihu.com/p/35509593) helps another time

### then install pytorch
only one instruction

but before that, install anaconda is a hard thing cause the download is so slow in China

so we can use the mirror in THU:)

do not forget the environment of anaconda

then
```
conda install pytorch torchvision cuda80 -c soumith
```

## well done


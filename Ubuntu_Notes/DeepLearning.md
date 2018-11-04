# Tensorflow Install and Google cloud platform configuration
## Tensorflow on Lenovo
First of all, have a look on tensorflow official website [Tensorflow install guide](https://www.tensorflow.org/install/install_linux?hl=zh-cn#NVIDIARequirements)
### Install Nvidia driver

### Install Cuda
- GTX940M + cuda 9.0 + cuDNN 7.0
- [A chinese guide](https://blog.csdn.net/qq_35976351/article/details/79325476)
- **Attention!** Must make sure each version of software that you installed
### Install cuDNN

### Install tensorflow python module
- Just follow the guide on the tensorflow website instructions
- Set up the virtual environment and then install, nothing special

## Google cloud platform
### Account register + VM apply
See the `.pdf` file *google_cloud_tutorial_i2dl.pdf*.
### ssh connection
- Here is a chinese tutorial for beginner to start the ssh connection.[Jianshu Tutorial](https://www.jianshu.com/p/57e85cf3e50b)
- By the way, the first two steps is not on your local computer, but on the google cloud VM, which you can open it through a button under the *ssh*
### install *gcloud sdk*
- It is necessary for uploading the file onto the google cloud VM. In order to install cuDNN later. 
- Download the install file from the official [GCloud tutorial](https://cloud.google.com/sdk/docs/?hl=zh-cn#Getting_Started)
- Also useful and detailed [document](https://ephrain.net/gcp-%E4%BD%BF%E7%94%A8-gcloud-%E9%80%A3%E7%B7%9A%E5%88%B0-google-cloud-platform-%E4%B8%8A%E7%9A%84-vm/)
### Install nvidia driver and cuda
- 这块其实有点含糊，tum info的pdf教程给的是`sudo apt-get install nvidia-cuda-toolkit`，完事之后，`nvidia-smi`就出来了，此时似乎不用再装cuda9.0，不然会出现驱动和lib不匹配，应该明确，tum的教程其实是为了后续给pytorch用，而非tensorflow
- [Taiwainese Tutorial](https://medium.com/@kstseng/%E5%9C%A8-google-cloud-platform-%E4%B8%8A%E4%BD%BF%E7%94%A8-gpu-%E5%92%8C%E5%AE%89%E8%A3%9D%E6%B7%B1%E5%BA%A6%E5%AD%B8%E7%BF%92%E7%9B%B8%E9%97%9C%E5%A5%97%E4%BB%B6-1b118e291015) Or just follow this tutorial, install cuda directly and cudnn
### tensorflow install
- Still follow the tensorflow official website install toturial. Since right now the VM is just an Ubuntu computer, all the same except it is on the server.


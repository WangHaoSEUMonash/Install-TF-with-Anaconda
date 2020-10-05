# Install-TF-with-Anaconda (written on Oct 2nd, 2020)
## Install tensorflow with Anaconda
* Install Anaconda
  * Download Anaconda3-2020.02-Windows-x86_64.exe on [Tsinghua University's mirror](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/)
  * Click "(Welcome to ...)Next", "I Agree", "(Select Installation Type)Just Me, Next", "(Choose Install Location)Next", (Advanced Installation Options, just mark the second one), "Next","Finish"
  * enviroment variable (EV)
    * In System Variable, New a EV named ANACONDA_HOME, whose path is the Anaconda installation path
    * In Enviroment Variable, add the three EVs into the "Path", whose names are "%ANACONDA_HOMES%\Scripts", "%ANACONDA_HOME%", "%ANACONDA_HOME%\Library\bin"
  * Confirm whether the Anaconda installation is sucessful
    * In cmd, type in "conda --version". If the version of Anaconda is given, it is successful.
  * **THIS IS THE END OF INSTALLING ANACONDA**

* Install tensorflow (TF)
  * In cmd, type in "conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/" and "conda config --set show_channel_urls yes"
  * Open Anaconda Prompt
  * Type in "conda create -n EnvName python=3.7" and type in "y"
  * Waiting until finish
  * Confirm whether the virtual enviroment installation is successful
    * Type in "conda info --envs" in Anaconda Prompt
  * Install TF
    * Type in "conda activate EnvName" in the (base)env.
    * In the (EnvName)env, type in "pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple/ tensorflow==1.xx(or 2.xx)" (In Andrew Ng's deep learning course homework, I choose 1.14) and wait
  * Confirm whether the TF installation is successful
    * Open Anaconda Prompt, enter the (EnvName)env
    * Type in "python", "import tensorflow as tf" 
  * **THIS IS THE END OF INSTALLING TF**

* Making the TF can be used in Jupyter notebook
    * Up to now, the TF can be used in Anaconda Prompt. However, when using it in Jupyter notebook, there is something wrong.
  * In the (EnvName)env, type in "conda install ipython" and "conda install jupyter"
  * Type in "ipython kernelspec install-self --user" and you can see sth like "Installed kernelspec python3 in C:\Users\xxx\Jupyter\kernels\python3"
  * Open Jupyter notebook and type in "import tensorflow as tf"
  * **CONGRADULATION that you have succedd installing TF on Anaconda**
  
## Reference
#### This direction is based on the two Chinese blogs as follows, thanks for the shared experience of the blogs' writers.
#### https://www.cnblogs.com/bjxqmy/p/12661931.html
#### https://blog.csdn.net/weixin_41043240/article/details/79519118

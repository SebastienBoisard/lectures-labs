# Deep Learning class - installation instructions

Download the Anaconda distribution for your Operating System
(Windows, macOS or Linux):

   - https://www.continuum.io/downloads (~400 MB)
   - Choose **Python 3.5**
   - Choose "64-bit installer"

Follow the instructions of the Anaconda page to install anaconda
on your laptop.

Create an environment for this class: 

    conda create --name env_m2dsupsdlclass python=3.5
     
Activate this new environment:

    conda activate env_m2dsupsdlclass

Open a console / terminal and update the following packages with conda:

    conda install python=3.5 numpy scikit-learn=0.18.1 jupyter matplotlib pip
    conda install pandas h5py pillow lxml

Install the tensorflow (without GPU support) and keras deep learning
libraries:

    pip install tensorflow==0.12.1 keras==1.2.1

Check that you can import keras with the python from anaconda:

    python -c "import keras; print(keras.__version__)"
    Using TensorFlow backend.
    1.2.1

Finally, launch jupyter notebook:

    IP_ADDRESS=`ip addr | grep 'state UP' -A2 | tail -n1 | awk '{print $2}' | cut -f1  -d'/'`
    jupyter notebook --ip=$IP_ADDRESS --no-browser


# Troubleshooting 

In a console check the installation location of the conda command in
your PATH:

    conda info

Read the output of that command to verify that your conda command is
associated with Python 3.5.


Check that the pip command in your PATH is the one installed by conda:

    pip show pip

In particular, look at the "Location:" line of pip is a subfolder
of the "environment root:" line from "conda info".

If you cannot solve your installations without the help of fellow students,
please feel free to send an email to the instructors with the outputs of the
previous command and include the full error messages along with the name and
version of your operating system.


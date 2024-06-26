In the next step, we use a Dask cluster in the cloud. One option for doing so, is to use [coiled.io](https://www.coiled.io/). 
Coiled can be used with AWS, Azure or a GCP account. The advantage is that one does not have to bother about the installation of the infrastructure for scaling. 
**Disclaimer:** I do not work for coiled nor is this is advertisement :blush:.

Till recently, it was possible to use Microsoft's Planetary Computer but this option has been stopped (please see Github discussion [here](https://github.com/microsoft/PlanetaryComputer/discussions/347)),

The installation nodes are based on the coiled.io documentation ([here](https://docs.coiled.io/user_guide/setup/index.html)) and [here](https://youtu.be/12mnkIYSekk) and [here](https://docs.coiled.io/user_guide/setup/aws/manual.html). The latter is for the manual installation. In the steps below, we document the automated installation and use Amazon Web Services (AWS) as the cloud provider at the backend. Other options are the Google Cloud Platform ([GCP](https://docs.coiled.io/user_guide/setup/gcp/cli.html)) or [Azure](https://docs.coiled.io/user_guide/setup/azure/cli.html).

The steps below are done a Windows 10 computer. 

## 1. Prerequisites - Please skip to part 2 if you have this already. 

### a. Python (Miniconda or Ananaconda) installation

TO ADD - Video of Quisheng Wu class

### b. Sign up for an Amazon Web Services (AWS) account. 

The steps for setting up an AWS account can be found in the [AWS documentation](https://docs.aws.amazon.com/SetUp/latest/UserGuide/setup-AWSsignup.html).

It is suggested to use the [AWS Free Tier account](https://aws.amazon.com/free/). 

It would suffice to stop at this step for installing coiled. In general, when installing AWS it is good practice not to work from your root account and create seperate users. This allows you to download AWS user credentials on your local computer. In step 3 (Connect to your cloud) below, the setup process would be slightly different in case you proceed creating a seperate user or not (and hence already have AWS credentials at this step here).

In case you want to create at this point of time your AWS credentials, first log into your [AWS (root) account](https://aws.amazon.com/console/). 

ADD IMAGE

Navigate to the 

## 2. Install coiled

It is advisable to create a virtual environment in Miniconda (or Anaconda). Open the **Anaconda Prompt** or **Terminal** and type `conda create -n coiledenv`. You can choose any other name other than coiledenv if you prefer as this is just an example. Press **Enter**:

TO ADD IMAGE

Activate the conda environment by typing: `conda activate coiledenv` and press **Enter**:

TO ADD IMAGE

Install (by using pip or conda) the coiled Python library:
```
pip install coiled "dask[complete]"
```
ADD IMAGE

If this gives an error like "", you need to install "pip" first, install pip first:

```
conda install pip
```


## 3. Connect to your cloud

In what next, we need to make a distinction whether you have already AWS credentials on your computer or not. If you would have AWS installation credentials already, this would look something like this in your home directory (e.g. C:\Users\yourusername). 

The other situation is that you do not have yet any of such credentials yet. Below, we make a distinction between having and not having AWS credentials (please see step 1 above).

### 3.1. Not having any AWS credentials.

### 3.2. Already having AWS credentials. 

   



 

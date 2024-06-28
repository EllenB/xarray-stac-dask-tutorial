In the next step, we use a Dask cluster in the cloud. One option for doing so, is to use [coiled.io](https://www.coiled.io/). 
Coiled can be used with Amazon Web Services (AWS), [Azure](https://docs.coiled.io/user_guide/setup/azure/cli.html) or the Google Cloud Platform ([GCP](https://docs.coiled.io/user_guide/setup/gcp/cli.html)) account. The advantage is that one does not have to bother about the installation of the infrastructure for scaling. 
**Disclaimer:** I do not work for coiled nor is this is advertisement :blush:.

Till recently, it was possible to use Microsoft's Planetary Computer but this option has been stopped (please see Github discussion [here](https://github.com/microsoft/PlanetaryComputer/discussions/347)),

Below, we use the AWS installation. The installation nodes are based on the coiled.io documentation [here](https://docs.coiled.io/user_guide/setup/index.html), [here](https://youtu.be/12mnkIYSekk) and [here](https://docs.coiled.io/user_guide/setup/aws/manual.html). The latter is for the manual installation. In the steps below, we document a semi-automated installation which should work whether you have already AWS keys installed on your system or have none installed. Below, we create a seperate user/AIM role for Coiled. 

The steps below are done a Windows 10 computer. 

## 1. Prerequisites - Please skip to part 2 if you have this already. 

### a. Python (Miniconda or Ananaconda) installation

The link to install Miniconda (which is more space consuming) can be found [here](https://docs.anaconda.com/miniconda/miniconda-other-installer-links/). 

If you prefer the larger installation, you can proceed with the [Anaconda installation]().

### b. Sign up for an Amazon Web Services (AWS) account. 

The steps for setting up an AWS account can be found in the [AWS documentation](https://docs.aws.amazon.com/SetUp/latest/UserGuide/setup-AWSsignup.html).

It is suggested to use the [AWS Free Tier account](https://aws.amazon.com/free/). This will install your root account for AWS. 

Optionally, you can protect this root account by using a Multi Factor Authentication (MFA). For more information, please see the [AWS documentation](https://aws.amazon.com/iam/features/mfa/) and [video](https://www.youtube.com/watch?v=e6A7z7FqQDE). 

## 2. Install coiled - THIS DOES NOT WORK YET - IN PROGRESS

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
TO ADD SCREENSHOT

Before creating the API token next, ensure that you are signed into Coiled (using your password you have created in the previous step).

Create the Coiled API token:

```
coiled login
```
ADD TWO IMAGES


### 3. Create a user in AWS

Login to your root account that you have just created under step 1 above:


## 4. Connect to your cloud

## 5. Trouble shooting

In some cases, the above steps may not work. The [video from Coiled]() may be useful in helping you troubleshoot. Alternatively, you may opt for a manual set-up. The steps are described on the Coiled website. 



   

# WMLA-notebook

## Create an Anaconda environment.

   * Navigate to Workload -> Spark -> Anaconda Management. If Anaconda3-2019-03-Linux-ppc64le is not listed, download it from this location: https://repo.continuum.io/archive/Anaconda3-2019.03-Linux-ppc64le.sh, then click Add and upload it.
   * Select Anaconda3-2019-03-Linux-ppc64le from the Anaconda Management page. Click Deploy.
   * Specify a name, for example, anaconda201903, and a deployment directory, such as /home/egoadmin/anaconda201903, for the Anaconda distribution.
   * Select the Environment Variables tab. Click Add Variable and add the following variables:
    IBM_POWERAI_LICENSE_ACCEPT=yes
    PATH=$PATH:/usr/bin or PATH=$PATH:/bin; based on where bash exists.
   * Click Deploy, then click Continue to Anaconda Distribution Instance.
   * In the Conda environments, click add
   * Select Create environment from a yaml file, click Browse, then select the powerai_1.6.1_anaconda2019.03.yml file and click Add.
   This creates a conda environment with the name powerAI161 with WML CE components installed in the environment. This powerAI161 conda environment will be configured with a Spark instance group in the following section.
   
## Deploy a spark instance group


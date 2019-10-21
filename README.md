# WMLA-notebook

## Create an Anaconda environment.

   * Navigate to Workload -> Spark -> Anaconda Management. If Anaconda3-2019-03-Linux-ppc64le is not listed, download it from this location: https://repo.continuum.io/archive/Anaconda3-2019.03-Linux-ppc64le.sh, then click Add and upload it.
   * Select Anaconda3-2019-03-Linux-ppc64le from the Anaconda Management page. Click Deploy.
   * Specify a name, for example, anaconda201903, and a deployment directory, such as /home/egoadmin/anaconda201903, for the Anaconda distribution.
   * Click Deploy, then click Continue to Anaconda Distribution Instance.<br>
   When anaconda environment is ready, click on Manage -> Configure (top right of the screen)
   * Click Add Variable and add the following variables:<br>
    IBM_POWERAI_LICENSE_ACCEPT=yes <br>
    PATH=$PATH:/usr/bin <br>
    <p align="center">
    <img src="https://github.com/regiscely/WMLA-notebook/blob/master/anaconda_variables.PNG" width="550" height="230">
    </p>
   * In the Conda environments, click add
   * Select Create environment from a yaml file, click Browse, then select the powerai_1.6.1_anaconda2019.03.yml file and click Add.
   This creates a powerai161 conda environment with WML CE components installed and extra packages (nvcc, jupyter) in the environment. 
   
## Deploy a spark instance group with powerai161 conda environment

   * Navigate to workload -> Spark -> Spark instance Group
   * Click "New" to create a new Spark Instance Group  
        <b>Required Fields</b>
        Instance group name: jupyter <br>
        Spark deployment directory: /var/conductor/jupyter <br>
        Execution user for instance group: egoadmin <br>
        Spark version: Spark 2.3.1 <br>
        Enable notebooks: Select Jupyter 5.4.0 <br>
             Anaconda distribution instance: anaconda201903 <br>
             Conda environment: powerai161 <br>
        
        <b>Consumers</b>
        Security:
             <i>leave default values</i>
        
        <b>Resource Groups and Plans</b>
          <i>select appriopriate resource groups</i>

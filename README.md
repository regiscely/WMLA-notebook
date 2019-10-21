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
        <b>Required Fields</b><br>
        Instance group name: <i><b>jupyter</b></i> <br>
        Spark deployment directory: <i><b>/var/conductor/jupyter</b></i> <br>
        Execution user for instance group: <i><b>egoadmin</b></i> <br>
        Spark version: <i><b>Spark 2.3.1 </b></i><br>
        Enable notebooks: Select <i><b>Jupyter 5.4.0 </b></i><br>
             Anaconda distribution instance: <i><b>anaconda201903</b></i> <br>
             Conda environment: <i><b>powerai161</b></i> <br>
        
        <b>Consumers</b><br>
        Security:
             <i>leave default values</i>
        
        <b>Resource Groups and Plans</b><br>
          <i>select appriopriate resource groups</i>
        <br>  
        Click <b><i>Create and deploy Instance Group</i></b> 
        Click <b><i>Continue to Instance Group</i></b> 
         
 ## Create Notebook for users
   * During Instance group deployment, click <b>"Notebooks"</b> tab 
   * Click <b>"Create Notebooks for User"</b> button
   * Select from users list, your current user id
   * Click <b>"Overview"<b> tab, a click <b>"start"</b> button to start your SIG
  
 ## import notebook to compile cupy
   * Navigate to workload -> Spark -> My application and notebooks
   * Select "Open Notebook" button (top right of the screen)
   * Select the notebook you created in previous steps
   
  

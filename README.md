# WMLA-notebook

Create an Anaconda environment.

   * Navigate to WorkloadSparkAnaconda Management. If Anaconda3-2018-12-Linux-ppc64le is not listed, download it from this location: https://repo.continuum.io/archive/Anaconda3-2018.12-Linux-ppc64le.sh, then click Add and upload it.
   * Select Anaconda3-2018-12-Linux-ppc64le from the Anaconda Management page. Click Deploy.
   * Specify a name, for example, myAnaconda, and a deployment directory, such as /home/egoadmin/myAnaconda, for the Anaconda distribution.
   * Select the Environment Variables tab. Click Add Variable and add the following variables:
    IBM_POWERAI_LICENSE_ACCEPT=yes
    PATH=$PATH:/usr/bin or PATH=$PATH:/bin; based on where bash exists.

   * Click Deploy, then click Continue to Anaconda Distribution Instance.


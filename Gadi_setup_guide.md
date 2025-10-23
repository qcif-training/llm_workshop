
## NCI Account Setup
Sign up for an  [NCI account](https://opus.nci.org.au/spaces/Help/pages/12583153/How+to+create+an+NCI+user+account)  if you don’t already have one.

Select  **Projects and groups**  from the left hand side menu and then select the  **Find project or group**  tab. Search for  **cd82**, the NCI-QCIF Training Partnership Project, and ask to join.
![](imgs/0_my_nci_project_cd82.png)

## NCI Australian Research Environment (ARE)

----------

Connect to  [NCI Australian Research Environment](https://are.nci.org.au/).

Be sure you use your NCI ID (eg, ab1234) for the username and not your email address.

Under  **Featured Apps**, find and click the  **JupterLab: Start a JupyterLab instance**  option.
![](imgs/0_nci_are_mainpage.png)

To Launch a JuptyerLab session, set these resource requirements:

| Resource                                 | Value                     |
| ---------------------------------------- | ------------------------- |
| Walltime (hours)                         | 5                         |
| Queue                                    | normal                    |
| Compute Size                             | small                     |
| Project                                  | cd82                      |
| Storage                                  | scratch/cd82              |
| Advanced Options…                        |                           |
| Modules                                  | python3/3.9.2             |
| Python or Conda virtual environment base | /scratch/cd82/venv_workshop |

Then click the Launch button.

This will take you to your interactive session page you will see that that your JupyterLab session is Queued while ARE is searching for a compute node that will satisfy your requirements.

Once found, the page will update with a button that you can click to Open JupyterLab.

Here is a screenshot of a JupyterLab landing page that should be similar to the one that opens in your web browser after starting the JupyterLab server on either macOS or Windows.



![](imgs/0_jupyterlab_landing_page.png)

## Transferring workshop notebooks

When you have a Jupyter server running use JupyterLab file navigator to go the folder that has the same name as your username. Then make a new Jupyter notebook by clicking on the “Python 3” icon under “Notebook” section and run the following code in a cell:

```
!rm -rf /scratch/cd82/$USER/notebooks
!mkdir -p /scratch/cd82/$USER/notebooks
!cp /scratch/cd82/regression_notebooks/* /scratch/cd82/$USER/notebooks/
!ls /scratch/cd82/$USER/notebooks/
```

And then use the Jupyter file browser to navigate to the directory:
/scratch/cd82/$USER/notebooks/ (where $USER is your NCI username)
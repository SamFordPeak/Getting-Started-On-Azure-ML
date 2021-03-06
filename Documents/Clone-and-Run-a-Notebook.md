# Clone and Run a Notebook

A lot of data science and machine learning experimentation is performed by running code in notebooks. Your compute instance includes fully featured Python and R notebook environments that you can use for extensive work (Jupyter, JuypyterLab and R Studio, more details in: [Creating and Running a Python or R Notebook](../Documents/Creating-and-Running-a-Python-Notebook.md)). But for basic notebook editing, you can use the built-in Notebooks page in Azure Machine learning studio.

1. In Azure Machine Learning studio, view the **Compute** page.

2. Your compute instance must be running. Select **JupyterLab** and then open a terminal session.
**Note:** This task can also be done using _Jupyter_ or _Terminal_ options that are also available in the Compute Instance. The process is very similar, so we will explain only how to do it in one of them, which, in this example, will be _JupyterLab_.

![](../Images/clonenotebook1.gif)

3. Double click on the `Users` folder and **right click** anywhere inside the folder to create a new folder with `your_username`

![](../Images/82.PNG)

Enter the commands shown below to clone a Git repository containing notebooks, data, and other files to your workspace:

` cd Users/<your_username>`

![](./Images/83.PNG)

 `git clone https://github.com/PeakIndicatorsHub/Getting-Started-On-Azure-ML`
 
![](../Images/84.PNG)
 
 4. When the command has completed, in the **My files** pane, click ↻ to refresh the view and verify that a new **Users/<user_name>/Getting-Started-On-Azure-ML** folder has been created. This folder contains several documents and folders. Double click the folder **labs**. This should contain multiple **.ipynb** notebook files.
 
![](../Images/Notebook4.gif)

**Note:** 
Because JupyterLab git version is not 2.8, we can't clone only the notebooks folder (git, prior to 2.8, doesn't support subfolders cloning). Therefore, the entire repository is cloned.

 ![](../Images/Notebook3.PNG)
 
 5. In the terminal pane, enter the following command to upgrade the Azure Machine Learning SDK and notebook widgets python packages to the latest version (these packages are used in most of the notebooks):
 
 ` pip install --upgrade azureml-sdk azureml-widgets`
 
 You may see some warnings as the package dependencies are installed. You can ignore these.
 
 6. Close the terminal pane, terminating the session.
 
 7. In the **Users/<user_name>/Getting-Started-On-Azure-ML/labs/**, open the **Getting_Started_with_Azure_ML.ipynb** notebook. Then read the notes and follow the instructions it contains to learn how to connect to your Azure ML workspace, view resources and run cells. 
 
  ![](../Images/Notebook4.PNG)
 
 **Tip:** To run a code cell, select the cell you want to run and then use the ▷ button to run it.

**Note:**
As stated before, the steps shown above demonstrate how to clone a gitHub repository using **JupyterLab** but once that clone is done the notebooks will be available within Azure Machine Learning Studio in every tool that allows access to a notebook (more details on the tools: [Creating and Running a Python or R Notebook](../Documents/Creating-and-Running-a-Python-Notebook.md)).

Below, we have an example where we can see that, even tought we use JupyterLab to clone the repository, the notebooks are accessible directly in Azure Machine Learning studio:
  ![](../Images/Notebook5.PNG)

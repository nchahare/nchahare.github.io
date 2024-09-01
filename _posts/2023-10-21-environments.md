---
layout: post
title: "Python: How to do environments"
description: Explanation of envirnonments in Conda and PIP
date: 2023-10-21
tags: resources
toc: true

authors:
  - name: Nimesh R. Chahare
    url: "https://nchahare.github.io"
    affiliations:
      name: Institute for Bioengineering of Catalonia, Barcelona
toc:
  - name: Introduction
  - name: Conda
  - name: No Conda
  - name: References
---

## Introduction

People commonly use Conda and Pip to manage their development environments and dependencies. 
- Conda, a powerful package manager and environment manager, provides a robust solution for creating isolated environments, installing packages, and managing dependencies not only for Python but also for other languages. It's particularly valuable in data science and scientific computing due to its cross-language support. 
- On the other hand, Pip, the Python package manager, is widely used for installing Python-specific packages. Together, Conda and Pip offer a comprehensive toolkit for developers, allowing them to effortlessly set up, manage, and share project-specific environments, making Python development more efficient and reproducible.

## Conda

Conda environments in Python are isolated workspaces that allow you to manage project-specific dependencies and isolate packages from your system-wide Python installation. Conda is a package manager and environment manager that provides a powerful way to create, manage, and switch between these environments. Here are the basics of Conda environments in Python:

1. **Creating a Conda Environment**:

   You can create a Conda environment using the `conda create` command. For example, to create a new environment named "myenv" with a specific Python version (e.g., Python 3.8), you can run:

   ```bash
   conda create --name myenv python=3.8
   ```

   This will create an isolated environment with the name "myenv" and install Python 3.8 within it.
   
   Or you can already have a file telling all the packages in `environment.yml`
   
```yaml
name: mycondaenv  # Name of the Conda environment
channels:       # Specify Conda channels for package sources
  - defaults
  - conda-forge

dependencies:   # List of package requirements
  - python=3.9  # Specify the Python version
  - numpy=1.21.1
  - pandas=1.3.1
  - scikit-learn=0.24.2
  - jupyter=1.0.0
  - matplotlib
  - requests
```

```bash
conda env create -f environment.yml
```

2. **Activating an Environment**:

   To use an environment, you need to activate it. The activation command depends on your operating system:

   - On Windows:

     ```bash
     conda activate myenv
     ```

   When an environment is activated, your command prompt or terminal should indicate the environment name, showing that you are working within that environment.

3. **Using Packages**:

   You can use Conda to install packages into the active environment. For example, you can install the Pandas library:

   ```bash
   conda install pandas
   ```

   This installs the Pandas library within the active environment. Packages installed in one environment do not affect other environments or your system-wide Python installation.

4. **Listing Installed Packages**:

   You can list the packages installed in the active environment using the following command:

   ```bash
   conda list
   ```

   This provides a list of installed packages and their versions.

5. **Deactivating an Environment**:

   To exit an environment and return to the base (system-wide) environment, you can deactivate it with the following command:

   ```bash
   conda deactivate
   ```

6. **Exporting and Creating Environment Files**:

   You can export the environment's configuration to a file using the `conda list --export` command. For example:

   ```bash
   conda list --export > environment.yml
   ```

   This creates an `environment.yml` file, which you can share with others or use to recreate the environment.

7. **Creating an Environment from a File**:

   You can create a new environment from an environment file using the `conda env create` command. For example:

   ```bash
   conda env create -f environment.yml
   ```

   This command creates a new environment based on the package specifications in the `environment.yml` file.

Conda environments provide a powerful way to manage dependencies and create isolated development environments for different projects. They are particularly useful for data science and scientific computing projects where different projects may require different versions of libraries and tools.

#### Delete the conda environments

You can delete Conda environments that you no longer need. Deleting environments can help free up disk space and keep your Conda environment list clean. Here's how to delete a Conda environment:

1. **List Your Environments**:

   First, list your Conda environments to see which ones you have. Open your command prompt or terminal and run:

   ```bash
   conda env list
   ```

   This will display a list of your Conda environments along with their paths.

2. **Deactivate the Environment (if activated)**:

   If the environment you want to delete is currently activated, make sure to deactivate it. You can do this by running:

   ```bash
   conda deactivate
   ```

3. **Delete the Environment**:

   To delete a Conda environment, use the following command, replacing `myenv` with the name of the environment you want to delete:

   ```bash
   conda env remove --name myenv
   ```

   If the environment was created in a specific location, you can specify the full path to the environment instead of the name.

   **Example for a specific path**:

   ```bash
   conda env remove --prefix /path/to/environment
   ```

   **Note**: Deleting an environment is permanent and cannot be undone. Make sure you want to delete the environment before proceeding.

Once you've run the `conda env remove` command, the specified environment will be permanently deleted from your system.

Always be careful when deleting environments, especially if they contain important data or configurations. It's a good practice to back up any critical data or settings before deleting an environment to avoid accidental data loss.


## No Conda

You can create and activate Python virtual environments using `venv` or `Conda`. For example, to create a virtual environment using `venv`:

   ```bash
   python -m venv myenv
   ```

   To activate the environment:

   ```bash
   .\myenv\Scripts\activate
   ```

Of course things will not work your way! You might get an error.

`because running scripts is disabled on this system. For more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.`

How to fix this?
- Go to powershell and run it as an admin
- Then, check your policy `Get-ExecutionPolicy`
- It will be restricted, so you change it to not restricted by entering `Set-ExecutionPolicy RemoteSigned` and `Y`
- The `RemoteSigned` execution policy allows the execution of scripts that are locally created and signed by a trusted publisher. You can also use other policies based on your security requirements, but `RemoteSigned` is a common choice.
- You should now be able to activate the virtual environment using the activation command (e.g., `.\myenv\Scripts\Activate`). 
- After you've finished your work with the virtual environment, you can set the execution policy back to its original state or to a more secure setting if needed. To do so, you can use the `Set-ExecutionPolicy` command with the desired policy, such as "Restricted" to revert to the default policy.

   To deactivate the environment:

   ```bash
   deactivate
   ```


#### To delete environments

`deactivate` the environment first

Then, `Remove-Item -Path .\env -Recurse`

#### Loading packages like environment.yml but with PIP

Here's an example of a `requirements.txt` file with Python package requirements:

```plaintext
# This is a comment
# You can use comments to provide explanations or notes

# Basic package requirements
numpy>=1.18.5  # Specific version of the NumPy library
pandas>=1.0.1  # Minimum required version of Pandas

# You can use operators to specify version constraints:
# - == for an exact version
# - >= for a minimum version
# - <= for a maximum version

# Additional packages
requests>=2.22.0
matplotlib>=3.2.0
scikit-learn
```

In this example:

- Lines starting with `#` are comments and are for documentation purposes.
- The `requirements.txt` file lists package requirements one per line.
- Package names are followed by optional version constraints to specify the required version. For example, `numpy==1.18.5` specifies that version 1.18.5 of NumPy is required, while `pandas>=1.0.1` specifies that a minimum version of Pandas 1.0.1 is required.
- You can use operators such as `>=`, `<=`, and ` == ` to specify version constraints.
- If you don't specify a version constraint, it means any version can be installed. For example, `scikit-learn` is listed without a version constraint, so any compatible version will be installed.

Once you have created or obtained a `requirements.txt` file, you can use it to install the specified packages or recreate a Python environment with the same package versions by running the following command:

```bash
pip install -r requirements.txt
```

This command will read the `requirements.txt` file and install the listed packages with their specified versions or constraints.

To create a Python virtual environment based on the requirements listed in a `requirements.txt` file, add additional packages to that environment using `pip`, and then save the updated requirements to a `requirements.txt` file, you can follow these steps:

To create a virtual environment based on these requirements, run the following command:

```bash
python -m venv myenv  # Create a new virtual environment
.\myenv\bin\activate  # Activate the virtual environment
pip install -r requirements.txt  # Install the initial package requirements
```

This creates a virtual environment named "myenv" and installs the packages listed in the `requirements.txt` file.

Once the virtual environment is activated, you can use `pip` to add more packages to it. For example, let's add the `requests` and `beautifulsoup4` packages:

   ```bash
   pip install requests beautifulsoup4
   ```

These packages will be installed into the active virtual environment.

To save the updated package requirements, run the following command while still in the virtual environment:

   ```bash
   pip freeze > updated_requirements.txt
   ```

This will create a new `updated_requirements.txt` file that includes all the packages, both the original ones from `requirements.txt` and the additional ones you installed.

Now, you have the `updated_requirements.txt` file that reflects the current state of the virtual environment, including the added packages. This file can be shared with others, used for documentation, or to recreate the environment exactly as you have it.

## References


[https://www.youtube.com/watch?v=1VVCd0eSkYc](https://www.youtube.com/watch?v=1VVCd0eSkYc)
Master the basics of Conda environments in Python
Great video to explain conda environment and how to do things
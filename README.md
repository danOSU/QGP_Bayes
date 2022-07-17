# QGP_Bayes
### Bayesian parameter estimation code for Relativistic Heavy Ion Collisions

1. Clone the repository to your local computer.
>git clone https://github.com/danOSU/QGP_Bayes.git
2. Please use environment.yml provided to generate a compatible conda environment.\
For more information please refer to *[Conda documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)* 
>conda env create --file environment.yml\
>conda activate QGP_Bayes\
>jupyter notebook --browser=safari\

3. Test to check if notebook runs properly.

You should be able to reproduce the following posteriors by selecting *run all* option in the notebook.

# Posteriors using this *[Jupyter Notebook](https://github.com/danOSU/QGP_Bayes/blob/main/Bayesian%20Parameter%20Estimation%20for%20Relativistic%20Heavy%20Ion%20Physics.ipynb)*
> Posterior for temperature dependent QGP specefic Shear viscosity.
![alt text](https://github.com/danOSU/QGP_Bayes/blob/main/Test/shear_pos_uniform_prior.png)

> Posterior for temperature dependent QGP specefic Bulk viscosity.
![alt text](https://github.com/danOSU/QGP_Bayes/blob/main/Test/bulk_pos_uniform_prior.png)

> Posterior for remaining parameters in the model.
![alt text](https://github.com/danOSU/QGP_Bayes/blob/main/Test/JETSCAPE_bayespartial.png)


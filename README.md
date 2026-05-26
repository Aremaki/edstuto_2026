# eds-tutorial

## About

In this tutorial we introduce some issues related to the analysis of real world data that are made available for research in **clinical data warehouses**. It is targeted towards data scientists that master the basics of Python programming and data analysis. The tutorial is decomposed in a series of small exercises and a final project. Whereas small exercises illustrate specific issues, the final project mimics an end-to-end research study that may be reported in a scientific article.

Data is fake, and this project can consequently be freely shared without impacting patients’ privacy. A fake data generator is made available and can be tuned to illustrate various use cases. Its development has been freely inspired by the characteristics and issues observed while analyzing data of the Greater Paris University Hospitals.


## Getting started

### Environment and kernel creation

Python, JupyterLab and an environment manager are recommended. You may choose for instance [Anaconda](https://docs.anaconda.com/anaconda/install/index.html).

We also recommend using Visual Studio Code.

Please follow theses instructions:
1. Open a terminal 
2. Go to your local repository for the 2025_EI project
3. Clone the project locally :
`git clone {URL}`
4. Using the terminal, access the cloned file
`cd edstuto`
5. Install the required packages with [uv](https://docs.astral.sh/uv/):
- `pip install uv==0.7.8`
- `uv venv --python 3.11.9`
- `source .venv/bin/activate`
- `uv sync`

NB: For VS Code users, in order to see clearly the plots, it is recommended to enable the Theme Matplotlib Plots in your setting > Extensions > Jupyter.

### Scientific libraries installation

The following scientific libraries developed in the context of Paris’ clinical data warehouse may moreover be leveraged to facilitate the resolution of some exercises:
- [eds-scikit](https://pypi.org/project/eds-scikit/): a set of tools to assist data scientists working on a clinical data warehouse (structured data).
- [edsnlp](https://pypi.org/project/edsnlp/): a set of spaCy components that are used to extract information from clinical notes written in French (unstructured data).


## Acknowledgement

We would like to thank [Assistance Publique – Hôpitaux de Paris](https://www.aphp.fr/)
and [AP-HP Foundation](https://fondationrechercheaphp.fr/) for funding this project.
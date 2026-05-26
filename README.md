# eds-tutorial

## About

In this tutorial we introduce some issues related to the analysis of real world data that are made available for research in **clinical data warehouses**. It is targeted towards data scientists that master the basics of Python programming and data analysis. The tutorial is decomposed in a series of small exercises and a final project. Whereas small exercises illustrate specific issues, the final project mimics an end-to-end research study that may be reported in a scientific article.

Data is fake, and this project can consequently be freely shared without impacting patients’ privacy. A fake data generator is made available and can be tuned to illustrate various use cases. Its development has been freely inspired by the characteristics and issues observed while analyzing data of the Greater Paris University Hospitals.


## Getting started

We recommend using **Visual Studio Code**.

### 1. Open a terminal

In VS Code, open a new terminal:

- Click on **Terminal > New Terminal**
- Or press **Ctrl + ù**
---

### 2. Install Git

First, check whether Git is already installed:

```bash
git --version
```

If the command does not work, install Git using one of the following commands.

#### Windows

In PowerShell:

```powershell
winget install --id Git.Git -e --source winget
```

#### macOS

If you use Homebrew:

```bash
brew install git
```

#### Ubuntu/Debian Linux

```bash
sudo apt update
sudo apt install git
```

After installation, close and reopen the terminal, then verify:

```bash
git --version
```

---

### 3. Install uv

`uv` will be used to install the correct Python version and the project dependencies.

#### Windows PowerShell

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/0.11.16/install.ps1 | iex"
```

#### macOS/Linux

```bash
curl -LsSf https://astral.sh/uv/0.11.16/install.sh | sh
```

Then close and reopen the terminal, and check:

```bash
uv --version
```

---

### 4. Clone the project locally

```bash
git clone https://github.com/Aremaki/edstuto_2026.git
cd edstuto_2026
```

---

### 5. Install Python and dependencies with uv

```bash
uv python install
uv sync --locked
```

This will create a local virtual environment in the `.venv` folder and install all required dependencies.

---

### 6. Select the Python environment in VS Code

In VS Code:

1. Open the Command Palette:

   * **Ctrl + Shift + P** on Windows/Linux
   * **Cmd + Shift + P** on macOS

2. Search for:

```text
Python: Select Interpreter
```

3. Select the interpreter located in the project folder:

---

### 7. Select the Jupyter kernel

When opening a notebook in VS Code:

1. Click **Select Kernel** in the top-right corner.
2. Choose the Python environment from the `.venv` folder.

If the `.venv` kernel does not appear, run:

```bash
uv run python -m ipykernel install --user --name edstuto_2026 --display-name "Python (edstuto_2026)"
```

Then restart VS Code and select the kernel again.

---

### Note for VS Code users

To see plots more clearly in notebooks, it is recommended to enable:

```text
Settings > Extensions > Jupyter > Theme Matplotlib Plots
```

### Scientific libraries installation

The following scientific libraries developed in the context of Paris’ clinical data warehouse may moreover be leveraged to facilitate the resolution of some exercises:
- [eds-scikit](https://pypi.org/project/eds-scikit/): a set of tools to assist data scientists working on a clinical data warehouse (structured data).
- [edsnlp](https://pypi.org/project/edsnlp/): a set of spaCy components that are used to extract information from clinical notes written in French (unstructured data).


## Acknowledgement

We would like to thank [Assistance Publique – Hôpitaux de Paris](https://www.aphp.fr/)
and [AP-HP Foundation](https://fondationrechercheaphp.fr/) for funding this project.
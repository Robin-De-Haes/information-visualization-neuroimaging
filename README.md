# Visualising a multi-modal neuroimaging dataset

Project of Group 8 for the Information Visualization course at [VUB](www.vub.be).

## 0. Contact information

Monty Python and the Three WISE Men:

| Name                     | Student number | Email address                                                      |
| :----------------------- | :------------- | :----------------------------------------------------------------- |
| Robin De Haes            | 0547560        | [robindehaes@msn.com](mailto:robindehaes@msn.com)                |
| Wolf De Wulf             | 0546395        | [wolf.de.wulf@ed.ac.uk](mailto:wolf.de.wulf@ed.ac.uk)              |
| Alexis François Verdoodt | 0545813        | [alexis.francois.verdoodt@vub.be](alexis.francois.verdoodt@vub.be) |

## 1. Data

Download the [preprocessed data](https://drive.google.com/file/d/10qr_cQ5pq_0PWN2rNVQxPtDGPDFYM56a/view?usp=sharing) (7.1G) and extract it into the existing `data` directory (to get a `data/processed` directory with 16 subject folders and a metadata.json file).  
The code that was used to process the data can be found in [data/preprocessing](data/preprocessing).  
Note that, because of the size of the dataset (+85GB), all preprocessing was run on the [VUB Hydra HPC](https://hpc.vub.be/).

## 2. Installation

### Create a Python virtual environment
```console
python -m venv env
```

### Activate the environment

*Linux/Mac*
```console
source env/bin/activate
```

*Windows*
```console
.\\env\Scripts\activate
```

To deactivate, use:
```console
deactivate
```

### Install the requirements
```console
pip install -r requirements.txt
```

## 3. Usage

To boot the [Panel](https://panel.holoviz.org/) visualisation, use:

```console
panel serve visualisation/run.py
```

The visualisation can then be accessed at: http://localhost:5006/

To stop the application, press `Ctrl-c` in the console.  

Keep in mind that the visualisation was developed and tested in the Google Chrome browser.  
While we do not guarantee it to work in other browsers, issues should be limited to layout.  

A demonstration video of the visualisation in use can be found in the [demo](demo) directory.

## (4. For developers)

Use the above command with the ``--autoreload`` option to allow for live code updates.

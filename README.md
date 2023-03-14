# ICIP2023-EAM-model

This repository contains the implementation of the EAM model proposed in the paper titled ["Help, I Shrunk My Savings! Assessing the Carbon Reduction Potential for Video Streaming from Short-Term Coding Changes"](https://research-information.bris.ac.uk/en/publications/help-i-shrunk-my-savings-assessing-the-carbon-reduction-potential) by Daniel Schien, which has been submitted to ICIP 2023. The EAM model is built on top of the eam-core library which is available at https://github.com/sust-cs-uob/eam-core.

## Repository files

- `groupings.yml`: This file contains the groupings used in the model to group time periods t_00 to t_23.
- `iplayer_views_per_hour.xlsx`: This file contains the hourly views data for iPlayer programs.
- `short_term_model.xlsx`: This file contains the input data required for running the short-term model.
- `short-term-model.yml`: This file contains the configuration for the short-term model used in the EAM model.
- `results/`: This directory will be created automatically when the model is run and will contain the output results.
  - `summary_v3.xlsx`: This file contains the summary of the output of the model.

## Installation

To use the EAM model, you need to have Python 3 installed on your system. You can install the required dependencies, including the eam-core library, by running the following commands in your terminal

Python 3:

```
sudo apt update
sudo apt install python3
python3 --version
sudo apt upgrade python3
```

eam-core:

```
git clone https://github.com/sust-cs-uob/eam-core.git
pip install -e .
```

ICIP2023 Model:

```
git clone https://github.com/sust-cs-uob/ICIP2023-EAM-model.git
```

## Running the model

To run the EAM model, execute the following command in your terminal:

```
eam-core -a ci -l -c ci -sd -a ci <path to short-term-model.yml>
```

NOTE: Depending on your directory layout you might need to change the paths within the short-term-model.yml

The output results will be saved in the `results/raw/` directory.

## Citation format

For citation information, please see the [CITATION.cff](./CITATION.cff) file.

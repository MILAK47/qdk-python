[![Build Status](https://dev.azure.com/ms-quantum-public/Microsoft%20Quantum%20(public)/_apis/build/status/microsoft.qdk-python?branchName=main)](https://dev.azure.com/ms-quantum-public/Microsoft%20Quantum%20(public)/_build/latest?definitionId=32&branchName=main)

# QDK-Python

## Introduction

QDK-Python is the repository for Python packages of the Quantum Development Kit (QDK). Currently, this consists of the following packages:

- `qdk` [![PyPI version](https://badge.fury.io/py/qdk.svg)](https://badge.fury.io/py/qdk)
- `azure-quantum` [![PyPI version](https://badge.fury.io/py/azure-quantum.svg)](https://badge.fury.io/py/azure-quantum)

Coming soon:

- qsharp

## Installation and getting started

To install the packages, we recommend installing the Anaconda Python distribution. For instructions on installing Conda on your system, please follow the [Conda user guide](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html).

To install the QDK package, run

```bash
pip install qdk
```

To install the Azure Quantum package, run

```bash
pip install azure-quantum
```

To get started running examples, start a Jupyter notebook:

```bash
cd examples
jupyter notebook
```

## Development

Install pre-reqs:

```bash
pip install azure_devtools pytest pytest-azurepipelines pytest-cov
```

To create a new Conda environment, run:

```bash
conda env create -f environment.yml
```

in the root directory of the given package (`qdk` or `azure-quantum`).

Then to activate the environment:

```bash
conda activate <env name>
```

where `<env name>` is the environment name (`qdk` or `azurequantum`).

To install the package in development mode, run:

```bash
pip install -e .
```

## Contributing

For details on contributing to this repository, see the [contributing guide](https://github.com/microsoft/qdk-python/blob/main/CONTRIBUTING.md).

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

### Note on Packages

While we encourage contributions in any part of the code, there are some exceptions to take into account.
- The package `azure.quantum._client` is autogenerated using the [Azure Quantum Swagger spec](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/quantum/data-plane). No manual changes to this code are accepted (because they will be lost next time we regenerate the client).
- The package `qdk.chemistry._xyz2mol` is maintained [here](https://github.com/jensengroup/xyz2mol) and included as a vendor package in this repo. Please make any suggestions or improvements to the code there.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.

# python-homewizard-energy

Asyncio package to communicate with HomeWizard Energy devices
This package is aimed at basic control of the device. Initial setup and configuration is assumed to done with the official HomeWizard Energy app.

## Disclaimer

This package is not developed, nor supported by HomeWizard.

## Installation
```bash
python3 -m pip install python-homewizard-energy
```

# Usage
Instantiate the HWEnergy class and access the API.

For more details on the API see the official API documentation on
https://homewizard-energy-api.readthedocs.io

## Example
```python
import asyncio
from homewizard_energy import HomeWizardEnergy

IP_ADDRESS = "192.168.1.123"


async def main():

    async with HomeWizardEnergy(host=IP_ADDRESS) as api

    print(await api.device())
    print(await api.data())

    await api.state_set(power_on=True)


asyncio.run(main())
```

# Development and contribution
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Requirements
- Python 3.9 or higher
- [Poetry](https://python-poetry.org/docs/#installing-with-pipx)

## Installation and setup
```bash
poetry install
poetry shell
pre-commit install
```

You can now start developing. The pre-commit hooks will run automatically when you commit your changes. Please note that a failed pre-commit hook will prevent you from committing your changes. This is to make sure that the code is formatted correctly and that the tests pass.

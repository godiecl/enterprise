# The Notes

## Conda

- Create a Conda environment: `conda env create -f environment.yml`

```yml
# the name of the environment
name: bremen
# channels from which to install packages
channels:
  - conda-forge
  - defaults
# packages to install (conda)
dependencies:
  - python=3.12
  - pip=24.0
  - opencv=4.9.0
# packages to install (pip)
  - pip:
      - coloredlogs==15.0.1
      - openpyxl==3.1.2
      - pandas==2.2.1
      - python-dotenv==1.0.1
      - pycodestyle==2.11.1
```

## Accounts

- Create a user: `useradd --base-dir /home/academicos --comment "<academic name>" --create-home --shell /bin/bash <account name>`
- Add superuser powers (optative): `usermod -aG sudo <account name>`
- Add to the `academicos` group: `usermod -aG academicos <account name>`
- Add to the `anaconda` group: `usermod -aG anaconda <account name>`
- Change the password: `passwd <account name>`

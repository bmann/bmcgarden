---
---

- [[Vyper]] smart contract language on [[ChromeOS]]
- Installing Vyper
	- Go the main [Vyper install instructions](https://vyper.readthedocs.io/en/latest/installing-vyper.html).
- Follow the MacOS instructions. Assuming you have [ChromeBrew](/chromebook/chromebrew) installed, get ```virtualenv``` setup:
  - ```crew install virtualenv```
- Follow instructions for virtualenv setup:
  - ```sudo apt install virtualenv
  virtualenv -p python3.6 --no-site-packages ~/vyper-venv
  source ~/vyper-venv/bin/activate```
- Then follow installation:
  - ```
  git clone https://github.com/ethereum/vyper.git
  cd vyper
  make
  make test```
- These tests take a long time, and are not required.
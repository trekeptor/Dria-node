![image](https://github.com/user-attachments/assets/28d801d4-b863-4f55-af14-cdbcc65c10b4)

# Dria Node
* Official Guide + Windows Version: https://dria.co/join
* This guide is for Linux AMD (aka VPS)
* You can run on both `CPU-only` or `GPU` clouds or local systems

## 1- Install Dependecies
```console
# lshw
sudo apt install lshw

# Ollama
curl -fsSL https://ollama.com/install.sh | sh

source /root/.bashrc
```

## 2- Install Dria
```
curl -fsSL https://dria.co/launcher | bash

source /root/.bashrc
```

## 3- Setup Dria Node
```console
# Run a step by step nodesetup
dkn-compute-launcher setup

# Change node settings manually: wallet, models, api keys, network settings
dkn-compute-launcher settings
```
* Make sure you modified `Wallet`, `Models`, `API Keys` and **Save & Exit**
* `Wallet`: Enter your EVM wallet privatekey
* `Models` I picked:
  * `ollama`: Needs high specs since it's a local model, check [Model Requirements Guide](https://firstbatch.notion.site/DKN-Node-Specs-1a6fb2d195758077906fdb9c7c778764).
  * `gemini`: A google API with upto 1500 free requests daily, No cost, no high specs. Get your Google API [here](https://aistudio.google.com/app/apikey)
  * `OpenRouter` is an API, You can buy credits with crypto to use it, Get API [here](https://openrouter.ai/settings/keys).
* `API Keys`: Since I'm only using `gemini` annd `openrouter` models, then i only enter their APIs and skip others.

![image](https://github.com/user-attachments/assets/924a2081-7730-4d4b-9506-357f957476d4)

> To measure your models: `dkn-compute-launcher settings` > Models > Measure local models > Press `Enter`

## 4-Run Dria Node
```console
# Open a screen session to run it on background
screen -S dria

# Run Node
dkn-compute-launcher start
```

![image](https://github.com/user-attachments/assets/18aae8e8-93b3-4dfb-bfaf-93f4341b2cc1)

* You can minimze the screen with `CTRL+A+D`
* To open your screen again:`screen -r dria`

## 5- Create/Enter Invite Code
Run:
```bash
dkn-compute-launcher referrals
```
* Create your own referral code and enter mine for your own node: `yeDwejMIC7m3FtvM4vD5`

## 6- Earn Node-Keeper Role
Join [Discord](https://discord.gg/dria) and Fill the [Form](https://docs.google.com/forms/d/e/1FAIpQLSeK090ejc4dg5x1ztb_yAOxGz5o1V8JUqDa-o3AwV1Lq7NpMA/viewform
) to receive role

![image](https://github.com/user-attachments/assets/4850511f-e9f7-4d5a-9270-2a2613439cc1)

## 6- Check your points
Connect Node EVM wallet and Check your points

https://dria.co/edge-ai/my-node

#

### Node Commands Help
```bash
dkn-compute-launcher
```

### Uninstall Node
```bash
dkn-compute-launcher uninstall
```



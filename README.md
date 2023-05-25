[![PyPI version](https://badge.fury.io/py/freeGPT.svg)](https://badge.fury.io/py/freeGPT)
[![Downloads](https://static.pepy.tech/personalized-badge/freeGPT?period=month&units=international_system&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/freeGPT)
[![License](https://img.shields.io/badge/License-MIT-bright&green.svg)](LICENSE)
# freeGPT
A Python package that gives access to GPT3 &amp; GPT4 models for free.
<br>
*Get started by doing: `pip install freeGPT`*

## Source:
*Models with .web have internet access on.*
<br>
| Models            | Websites                                 |
| ----------------- | -----------------------------------------|
| gpt3              | [theb.ai](https://theb.ai)               |
| gpt3.web          | [you.com](https://you.com)               |
| gpt4              | [usesless.com](https://ai.usesless.com)  |
| gpt4.web          | [forefront.ai](https://chat.forefront.ai)|

### TODO-List:
- [x] Add GPT-4.
- [x] Make the library well-documented.
- [x] Make the over-all library easier to use.
- [x] Make the over-all library easier to understand.
- [x] Replace you.com with theb.ai for less failed responses.
- [ ] Add a internet search model for GPT-3 & GPT-4
- [ ] Make a discord bot
- [ ] Add text to image generation

## Examples:

#### GPT-3:

```python
from freeGPT import gpt3

def send_prompt():
    try:
        prompt = input("> ")
        response = gpt3.Completion.create(prompt=prompt)
        print("Response:", response.text)
    except Exception as e:
        print("Error:", str(e))

while True:
    send_prompt()
```
#### GPT-4:

```python
from freeGPT import gpt4

token = gpt4.Account.create(logging=True)
print("Token:", token) 

def send_prompt():
    try:
        prompt = input("> ")
        for response in gpt4.Completion.create(prompt=prompt, token=token):
            print("Response:", response.text)
    except Exception as e:
        print("Error:", str(e))

while True:
    send_prompt()
```

## Star History:
[![Star History Chart](https://api.star-history.com/svg?repos=Ruu3f/freeGPT&type=Date)](https://github.com/Ruu3f/freeGPT/stargazers)

## Support me:
- Join my [Discord Server](https://discord.gg/NcQ26PrNDp) :D
- Star this repository :D


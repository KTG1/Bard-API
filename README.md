Development Status :: 4 - Beta


# Google <a href="https://bard.google.com/"><img src="https://camo.githubusercontent.com/adb54264fe2ad5067d07d0752fc32600b4e6250073b01ce8c386575b431e3f06/68747470733a2f2f7777772e677374617469632e636f6d2f6c616d64612f696d616765732f66617669636f6e5f76315f31353031363063646466663766323934636533302e737667" height="20px"></a> Bard API 


<p align="left">
<a><img alt="PyPI package" src="https://img.shields.io/badge/pypi-BardAPI-black"></a>
<a href="https://pypi.org/project/bardapi/"><img alt="PyPI" src="https://img.shields.io/pypi/v/bardapi"></a>
<!-- <a href="https://pepy.tech/project/bardapi"><img alt="Downloads" src="https://pepy.tech/badge/bardapi"></a> -->
<a><img alt="commit update" src="https://img.shields.io/github/last-commit/dsdanielpark/Bard-API?color=black"></a>
<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
<a href="https://github.com/dsdanielpark/Bard-API"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdsdanielpark%2FBARD_API&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=bardapi&edge_flat=false"/></a></a>
</p>

> A package that returns Response of [Google Bard](https://bard.google.com/) through API

![](./assets/bardapi.gif)


I referred to [this github repository(github.com/acheong08/Bard)](https://github.com/acheong08/Bard) where inference process of Bard was reverse engineered. Using `__Secure-1PSID`, you can ask questions and get answers from Google Bard. This package is designed for application to the Python package [ExceptNotifier](https://github.com/dsdanielpark/ExceptNotifier) and [Co-Coder](https://github.com/dsdanielpark/Co-Coder). 

<br>

Never expose the `__Secure-1PSID` for your safety.
> Note that while I referred to `__Secure-1PSID` value as an API KEY for convenience, it is not an officially provided API KEY. 

<br>

##  [Amazing Bard Prompts](https://github.com/dsdanielpark/amazing-bard-prompts) Is All You Need!
- Helpful prompts for Google Bard

<br>

## Install
The latest stable release (and required dependencies) can be installed from PyPI:
```
pip install bardapi
```
You may instead want to use the development version from Github:
```
pip install git+https://github.com/dsdanielpark/Bard-API.git
```

<br>

## Authentication
1. Visit https://bard.google.com/
2. F12 for console
3. Session: Application → Cookies → Copy the value of  `__Secure-1PSID` cookie.

<br>

## Usage 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1YIMA8aBmEQSSk90bB0Q9tznaLLQcluGA?usp=share_link) 


Simple Usage
```python
from bardapi import Bard
import os

os.environ['_BARD_API_KEY']="xxxxxxxx"
Bard().get_answer("나와 내 동년배들이 좋아하는 뉴진스에 대해서 알려줘")['content']
```


Or you can use this
```python
import bardapi
import os

# set your __Secure-1PSID value to key
os.environ['_BARD_API_KEY']="xxxxxxxx"

# set your input text
input_text = "나와 내 동년배들이 좋아하는 뉴진스에 대해서 알려줘"

# Send an API request and get a response.
response = bardapi.core.Bard().get_answer(input_text)
```

Example
<br>

<a href="https://bard.google.com/"><img src="./assets/bardimg.png" height="600px">


<br>

## Scripts
In the scripts [folder](./scripts/), I have released a script to help you compare [OpenAI-ChatGPT](./scripts/openai_api.ipynb) and [Google-Bard](./scripts/google_api.ipynb). I hope they will help more developers.

## License
- [MIT](https://opensource.org/license/mit/) 
- I hold no legal responsibility; for more information, please refer to the bottom of the readme file. I just want you to give me and [them](https://github.com/acheong08/Bard) a star...


## Bugs and Issues
Sincerely grateful for any reports on new features or bugs. Your valuable feedback on the code is highly appreciated.

## Contacts
- Core maintainer: [Daniel Park, South Korea](https://github.com/DSDanielPark) <br>
- E-mail: parkminwoo1991@gmail.com <br>

## Reference 
[1] https://github.com/acheong08/Bard
  
### Important Warning: All legal responsibilities associated with the use of the package lie with the user.
The Python package `BardAPI` just provides code for Python developers to easily access Google Bard. All responsibility for handling data and using the package lies with the user. There is no monetary compensation received for the use of this code, and it should be noted that there is no liability for the use of the code. Please refer to the Google Bard Official Document for more details. 
  

#### Could you kindly add this badge to your repository?
markdown
```
![BardAPI](https://img.shields.io/badge/pypi-BardAPI-black)
```
html
```
<a href="https://github.com/dsdanielpark/Bard-API"><img alt="PyPI package" src="https://img.shields.io/badge/pypi-BardAPI-black"></a>
```
Thank you for your interest.

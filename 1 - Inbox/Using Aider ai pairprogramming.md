---
aliases: 
publish: true
created: 2023-10-26
modified: 2024-09-03T16:05:08+02:00
---
# Aider

A pairprogramming tool using openai's GPT3/GPT4. It's currently running on Python 3.11

## Installation

I had no luck porting it to nixos, so I went to install it via classic Python

```shell
python3 -m pip install aider-chat
```

## Usage

Adding the **openai** API key to *~/.aider.conf.yml*:
```yaml
openai-api-key: sk-...
```

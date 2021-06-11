
# `CRYPTROOPER`

A module that can endode and decode your text with your given key.


| ![LICENSE](https://img.shields.io/badge/License-Mozilla%20Public%20License%202.0-green.svg)| ![Tests](https://img.shields.io/badge/Tests-Passing-blue.svg) |
| :----- | :----- |
| ![Builds](https://img.shields.io/badge/Builds-Passing-blue.svg) | ![Maintainer](https://img.shields.io/badge/Maintainer-Parvat-black.svg) |

## Features

- No additinal installation required.
- Can work on any system with python >= 3.8
- Can encode and decode text of any language.
- Can encode and decode emoticons and symbols also.
## Installation 


Install cryptrooper with pypi

```bash
  pip install cryptrooper
```

## Documentation

`Crypto` is a class in the `__init__.py` file at the module `cryptrooper`.

#### Parameters:
- text 
    - The text you want to encode or decode.
- key
    - The key to encode or decode the text with.
#### Functions:
- encode
    - The function that encodes your text with your key.
    - returns a `DICT` like the below one:
        ```python
        {  
            "key": "Your Key",
            "encoded": "The encoded text",
            "decoded": "The decoded text",
            "result": "The encoded text",
            "error": None
        }
        ```
        - The error is None if no error, else it contains the class of raised error.

- decode
    - The function that decoded your encoded text with your key.
    - returns a `DICT` like the below one:
        ```python
        {  
            "key": "Your Key",
            "encoded": "The encoded text",
            "decoded": "The decoded text",
            "result": "The decoded text",
            "error": None
        }
        ```
        - The error is None if no error, else it contains the class of raised error.



Example of encoding:
```python
from cryptrooper import Crypto

# `Crypto` is a class.
text = "The text you want to encode."
key = "The key."


# passing the text and key to Crypto
ins = Crypto(text, key)


# getting the result which is of type `dict`
result = ins.encode()
print(result)


# this prints:
# {
#     'key': 'The key.',
#     'encoded': '168 208 202 64 223 202 241 200 \136 222 143 224 133 240 181 214 217 64 223 212 153 185 214 200 143 207 202 167',
#     'decoded': 'The text you want to encode.',
#     'result': '168 208 202 64 223 202 241 200 136 222 143 224 133 240 181 214 217 64 223 212 153 185 214 200 143 207 202 167',
#     'error': None
# }
```


Example of decoding:
```python
from cryptrooper import Crypto


# `Crypto` is a class.
text = "183 212 212 149 214 215 232 149 204 223 143 215 207 225 212 163"
key = "cloud"


# passing the text and key to Crypto
ins = Crypto(text, key)


# getting the result which is of type `dict`
result = ins.decode()
print(result)


# this prints:
# {
#     'key': 'cloud',
#     'encode': '183 212 212 149 214 215 232 149 204 223 143 215 207 225 212 163',
#     'decode': 'The sky is blue.',
#     'result': 'The sky is blue.',
#     'error': None
# }
```
## Authors

- [@Parvat-web-dev](https://www.github.com/Parvat-web-dev)
- [@Rohithsreedharan](https://www.github.com/Rohithsreedharan)

  

## Contributing

Contributions are always welcome!
Contact [*@Parvat_R*](https://telegram.me/Parvat_R) for Contributions.

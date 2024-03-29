# Information:

A useful feature for bot developers. Get information about the characters from the showcase, for their further use.
!!! tip "Requires ENC"
    This function requires an [enc()](enc.md) argument that must be obtained from the enc function

## Profile:
It takes ```enc``` and ```image``` argument.


```enc``` - The result returned by the ```EnkaGenshinGeneration().enc()``` function
```image``` - Generate a profile picture or not.

### Example
``` python
from enkanetworkcard import encbanner
import asyncio

ENC = encbanner.EnkaGenshinGeneration()
encR = asyncio.run(ENC.enc(uids = "811455610"))
resultProfile = ENC.profile(enc = encR, image = False)
print(resultProfile)
```

### Result:
```python
{"characters": {"name_charter": {...}, "charactersArg": {"name1", "name2", ..}, img: ...}
```

- ```characters``` - Information about each character.
- ```charactersArg``` - List of character names to quickly pass to ```start()```
- ```img``` - Showcase generated image.



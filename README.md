# jmd_imagescraper
> An image scraping library for creating deep learning datasets.


This library is for creating deep learning datasets. It uses DuckDuckGo for the image scraping as they have some rather nice parameters to make your life easier, for example we can filter the searches to only return photos, and only images which are (relatively) square.

Included is an image cleaner which you can use directly from your notebook to check the results and delete unsuitable images.

Also included is the ability to create CSV datasets which just contain a list of URLs and their labels.

## Install

`pip install jmd_imagescraper`

## How to use

```python
from pathlib import Path
from jmd_imagescraper.core import *

root = Path().cwd()/"images"

duckduckgo_search(root, "Puppies", "cute puppies", max_results=500)
```

    Duckduckgo search: cute puppies
    Downloading results into C:\Users\Joe\Documents\GitHub\jmd_imagescraper\images\Puppies
    



<div>
    <style>
        /* Turns off some styling */
        progress {
            /* gets rid of default border in Firefox and Opera. */
            border: none;
            /* Needs to be in here for Safari polyfill so background images work as expected. */
            background-size: auto;
        }
        .progress-bar-interrupted, .progress-bar-interrupted::-webkit-progress-bar {
            background: #F44336;
        }
    </style>
  <progress value='128' class='' max='500' style='width:300px; height:20px; vertical-align: middle;'></progress>
  25.60% [128/500 00:45<02:12 Images downloaded]
</div>



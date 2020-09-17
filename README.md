# jmd_imagescraper
> An image scraping library for creating deep learning datasets.


This library is for creating deep learning datasets. 

It uses DuckDuckGo for the image scraping as they have return nice big images and have some rather nice parameters to make your life easier, for example we can filter the searches to only return square images which are photos.

`jmd_imagescraper.core` contains the main scraping/downloading functionality. \
`jmd_imagescraper.imagecleaner` contains an image cleaner you can use from within your notebook to clean up the results and delete anything unsuitable.

## Install

`pip install jmd_imagescraper`

## How to use

```python
from jmd_imagescraper.core import *
from pathlib import Path

root = Path().cwd()/"images"
duckduckgo_search(root, "Puppies", "cute puppies", max_results=10)
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
  <progress value='10' class='' max='10' style='width:300px; height:20px; vertical-align: middle;'></progress>
  100.00% [10/10 00:02<00:00 Images downloaded]
</div>






    [WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/001.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/002.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/003.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/004.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/005.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/006.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/007.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/008.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/009.jpg'),
     WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images/Puppies/010.jpg')]



```python
from jmd_imagescraper.imagecleaner import *
display_image_cleaner(root)
```

![](image_cleaner.jpg)

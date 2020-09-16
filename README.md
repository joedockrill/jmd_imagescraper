# jmd_imagescraper
> An image scraping library for creating deep learning datasets.


This library is for creating deep learning datasets. It uses DuckDuckGo for the image scraping as they have some rather nice parameters to make your life easier, for example we can filter the searches to only return photos, and only images which are (relatively) square.

Included here is an image cleaner which you can use directly from your notebook to check the results and delete unsuitable images.

Also included is the ability to create CSV datasets which just contain a list of URLs and their labels.

## Install

`pip install jmd_imagescraper`

## How to use

```python
from pathlib import Path

root = Path().cwd()/"images"
root
```




    WindowsPath('C:/Users/Joe/Documents/GitHub/jmd_imagescraper/images')



```python
duckduckgo_search(root, "Puppies", "cute puppies", max_results=10)
```

    Duckduckgo search: cute puppies
    Downloading 10 results into C:\Users\Joe\Documents\GitHub\jmd_imagescraper\images\Puppies
    




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



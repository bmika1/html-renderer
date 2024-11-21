# render_html_v2

`render_html_v2` is a fork of the library render_html by bmika1 found here 
https://github.com/bmika1/render-html it keeps the api the same but gives you the option to include your own encoding.
It allows you to open HTML content directly from a string or save it to a file and open it from the file.
You can also specify the name of a browser to use a non-default browser. Please refer to [webbrowser documentation](https://docs.python.org/3/library/webbrowser.html) for the complete list of predefined browsers.
This library is especially useful for quickly visualizing and testing HTML content in a web browser environment.

## Installation

You can install `render_html_v2` using pip:

pip install render-html-v2

NOTE: the library requires Python 3.10 or newer

## Usage

```python
from render_html import render_in_browser as ren
import requests

# Making a request with the requests library
response = requests.get('https://example.com')

# Rendering the HTML response in the default browser
html_content = response.text
ren(html_content)
```

## Documentation

### `render_in_browser(html_string, save_path=None, browser=None, encoding=None)`

Render the HTML content in a web browser.

- `html_string` (str): The HTML content as a string.
- `save_path` (str, optional): The path to save the HTML content as a file.
  If provided, the HTML content will be saved to the specified file and opened from it.
  If not provided or set to `None`, a temporary file will be created in the operating 
  system's default temporary directory. The temporary file will be removed once the rendering 
  is complete.
- `browser` (str, optional): The name of the web browser to use (i.e., "chrome", "safari").
  If provided, the HTML content will be opened using the specified browser.
  If not provided or set to None, the default browser will be used.
- `encoding` (str, optional) the encoding method you want to encode your content
  If not provided, the default option will be chosen 



## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


# Court Data Standard Documentation

## Requirements
- Python >= 3.10
- pipenv >= 2022.10.11


## Setting Up the Environment

1. Create a virtual environment with `pipenv` and install dependencies by executing the following commands in a terminal or command prompt window.
   
```sh
pipenv sync
pipenv shell
```

1. To assemble new HTML documents from the source files, navigate to the `docs` directory and use the following command in a terminal instance or command prompt:

```sh
sphinx-build -b html source build
```

## Viewing documentation from the build

Sphinx generates HTML documents from the files located in the `/docs/source/` directory. This repository contains the most current generated HTML version of the source documents and can be viewed by navigating to http://localhost:8000/ in a web browser.

Start a local server. It will serve the contents of the specified directory on Port 8000.
  
```sh
python -m http.server --directory /path/to/built/docs
```
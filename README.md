# Court Data Standard Documentation

## Requirements
- Python >= 3.10
- pipenv >= 2022.10.11


## Setting Up the Environment

1. Create a virtual environment with `pipenv` and install dependencies by executing the following commands in a terminal or command prompt window.
   
  `pipenv sync`  
  `pipenv shell`
  
2. Start a local server. It will serve the contents of the current directory on Port 8000.
  
`pipenv run python -m http.server`

## Generating a Webpage From Source Documents

Sphinx generates HTML documents from the files located in the `/docs/source/` directory. This repository contains the most current generated HTML version of the source documents and can be viewed by navigating to `http://localhost:8000/docs/build/html/` in a web browser.

To assemble new HTML documents from the source files, navigate to the `docs` directory and use the following command in a terminal instance or command prompt:

`make html`


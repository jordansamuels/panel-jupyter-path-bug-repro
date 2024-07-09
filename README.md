This is a minimal repro of a bug in panel preview in Jupyter.

Steps to reproduce:
1. Have any recent conda or equivalent in your PATH, e.g. micromamba 1.5.8 on OSX
2. Run `make` in this directory.  This will
   * Make a new conda environment in `.venv` with panel and jupyter.
   * Start Jupyter Lab and open `repro.ipynb`.
4. Execute all cells in the notebook and confirm it works.
5. Enable panel preview -> this will result in an import error: `ModuleNotFoundError: No module named 'hello'`

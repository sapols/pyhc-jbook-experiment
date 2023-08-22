# PyHC Jupyter Book Gallery

This is a demo of using [Jupyter Book](https://jupyterbook.org/) for the [PyHC gallery](https://heliopython.org/gallery/generated/gallery/index.html)—a gallery of examples and tutorials for the Python in Heliophysics Community.

## Contributing
The process of adding a new example notebook to this gallery is trivially easy for PyHC members. It has not been automated yet, so the steps are simply: 

  1. Open a PR that adds your `.ipynb` notebook file to `book/src/`
  2. Shawn will take it from there

Shawn will do the work of updating the table of contents and the Python environment to make the new notebook executable. Any necessary discussion can happen inside the PR.

## Development Environment

Binder link: https://mybinder.org/v2/gh/sapols/pyhc-jbook-experiment/main?urlpath=lab/tree/book/src

Binder is the primary backend used for running the examples in this gallery. It builds the Python environment from the files stored in this repo's `binder/` directory. Note that we use a minimal set of dependencies needed to run the examples, which speeds up Binder load times. 

There exists a version of the Python environment with every published PyHC package, but the image is too large to work with Binder. Interested users are encouraged to try it out via the [`pyhc-gallery`](https://hub.docker.com/r/spolson/pyhc-gallery) Docker image in Docker Hub.

## Deployment

At present, this site is deployed manually through Netlify's web interface. We run `jupyter-book build .` locally, then deploy the generated `html` folder, basically. This process will soon be automated with GitHub Actions.
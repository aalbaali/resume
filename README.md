# LaTeX VSCode Workspace Container
- This is a template for running a LaTeX Docker container within VSCode workspace
- The code is forked from [this repo](https://github.com/qdm12/latexdevcontainer)
- It installs custom LaTeX packages from [this repo](https://github.com/aalbaali/latex_classes)

# Usage
- This is a Github template, so use the template to create a new repo
- Write `.tex` files and build (`ctrl + shift + b`)

# Running using Docker
## Build image
```bash
docker build -f Dockerfile -t latex_dev_image  .
```
where `latex_dev_image` is the image name, which can be replaced by another image.

## Build latex using non-interactive container
Run
```bash
docker run --rm -it -v $PWD:/home/latex/simple_tex -w=/home/latex/simple_tex  --user latex latex_dev_image  make
```
# TODOs
- Add latex snippets
- Add aliases
- Proper Github workflows

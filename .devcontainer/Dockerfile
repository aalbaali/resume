FROM aalbaali/latex:full

# This is the same Dockerfile used in aalbaali/latex-action

RUN DEBIAN_FRONTEND=noninteractive
RUN sudo sudo apt-get update -y \
        && sudo apt-get install -y \
            zathura      \
            okular       \
            mupdf        \
            xdotool

RUN DEBIAN_FRONTEND=

# Install the custom classes
RUN mkdir -p /tmp/custom_latex \
    && cd /tmp/custom_latex \
    &&  echo $(ls .) && echo "$PWD" \
    && wget -c https://raw.githubusercontent.com/aalbaali/latex_classes/master/install.sh?token=GHSAT0AAAAAABRI2OOT3SC4C7IOHDIQJ5K4YQRPABA -O install_tex.sh \
    && chmod +x install_tex.sh \
    && ./install_tex.sh

ENV TZ="Canada/Eastern"
RUN date

CMD ["bash"]

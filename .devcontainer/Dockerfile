FROM aalbaali/latex:dev

RUN DEBIAN_FRONTEND=noninteractive
RUN sudo sudo apt-get update -y \
        && sudo apt-get install -y \
            zathura      \
            okular       \
            mupdf        \
            xdotool      \
            wget         \
            texlive-full

ARG USERNAME=latex
USER $USERNAME

RUN echo "PWD: $PWD" \
    && echo "USERNAME: $USERNAME" \
    && echo "USER: $USER"

ENV CACHE=1

# Install the custom classes
RUN mkdir -p /home/$USERNAME/custom_latex \
    && cd /home/$USERNAME/custom_latex \
    &&  echo $(ls .) && echo "$PWD" \
    && wget -c https://raw.githubusercontent.com/aalbaali/latex_classes/master/install.sh?token=GHSAT0AAAAAABRI2OOT3SC4C7IOHDIQJ5K4YQRPABA -O install_tex.sh \
    && chmod +x install_tex.sh \
    && ./install_tex.sh


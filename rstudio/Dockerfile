FROM base/archlinux

RUN \
    pacman -Sy && \
    pacman -S archlinux-keyring --noconfirm && \
    pacman -S docker-compose openssl --noconfirm && \
    pacman -Scc --noconfirm

ADD docker-compose.yml startup.py requirements.txt .
RUN pip install -r requirements.txt
CMD python startup.py up
FROM jonathonf/manjaro

RUN mkdir -p /root/.gnupg \
 && touch /root/.gnupg/dirmngr_ldapservers.conf \
 && dirmngr < /dev/null \
 && pacman -Syy --noconfirm \
 && pacman-key --refresh-keys; \
    pacman-key --populate archlinux manjaro \
 && pacman -S archlinux-keyring manjaro-keyring --noconfirm \
 && pacman -Syyu --noconfirm \
 && pacman -Sc --noconfirm

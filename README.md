st - simple terminal
--------------------
This is a personal fork of [st][] with the following patches applied:

- [desktopentry][] ([diff][diff-1])
- [solarized][] ([diff][diff-2])


`st` is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build `st` you need the `xlib` header files:

```sh
sudo apt-get install libx11-dev
sudo apt-get install libxft-dev
```


Installation
------------
Edit `config.mk` to match your local setup (`st` is installed into
the `/usr/local` namespace by default).

Afterwards enter the following command to build and install `st` (if
necessary as `root`):

```sh
make clean install
```


Running st
----------
If you did not install `st` with `make clean install`, you must compile the
`st` `terminfo` entry with the following command:

    tic -sx st.info

See the `man` page for additional details.


Credits
-------
Based on Aurélien APTEL `<aurelien dot aptel at gmail dot com>` `bt` source
code.


[desktopentry]: https://st.suckless.org/patches/desktopentry/
[diff-1]:       https://st.suckless.org/patches/desktopentry/st-desktopentry-0.8.2.diff
[diff-2]:       https://st.suckless.org/patches/solarized/st-solarized-dark-20180411-041912a.diff
[solarized]:    https://st.suckless.org/patches/solarized/
[st]:           https://st.suckless.org/

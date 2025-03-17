# Compiz Reloaded ports for FreeBSD

Compiz Reloaded (https://gitlab.com/compiz) is supported for compiz-0.8.x series.

I have created FreeBSD ports for Compiz Reloaded.

You can download these files and overwrite ports tree, or use ports overlays method. I recommend using ports overlays method.

## ports overlay method

Add in your `/etc/make.conf` as follows:

`OVERLAYS+=/your/download/directory/compiz-related-ports`

If you use poudriere, you may need to add to `/etc/make.conf` as follows:

    .ifndef POUDRIERE_BUILD_TYPE
    OVERLAYS+=/your/download/directory/compiz-related-ports
    .endif

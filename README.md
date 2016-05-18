# mutt-patched-arch
Mutt E-mail client with some patches I'm using.

The package name by default is: `mutt-sidebar-x-gm-labels` (not to be confused with other AUR packages, like _mutt-sidebar_ which doesn't contain the X-GM-LABELS patch.)

#### Patches:
* trash folder support
* [sidebar](http://www.lunar-linux.org/mutt-sidebar/)
* first char in mailboxdir
* shortpath
* Gmail's X-GM-LABELS support - for displaying gmail labels in the e-mail list (index_format). Works only via IMAP connection.

#### Installation:

* To install the compiled package, run:

`sudo pacman -U /path/to/mutt-sidebar-x-gm-labels-1.5.23-10-x86_64.pkg.tar.xz`

(by default it's in the **compiled_package** directory)

* If you want to compile the package, or change it's name, or remove a patch from it, etc., edit the **PKGBUILD** first, then run `makepkg` in the same directory (where the PKGBUILD and all the other files are). After it's finished, run: `sudo pacman -U /path/to/your-compiled-mutt.pkg.tar.xz`

#### Enable Gmail labels in the e-mail list (index_format):

In your **.muttrc** add this to the **index_format**: ` %?y?(%y)?`

Or, you can add this instead: `[%-15.15y]` to show brackets around the labels.

If the labels won't show up (or they won't get refreshed), make sure you disable the `header_cache` (do **NOT** `set header_cache`)





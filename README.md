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

Go to the cloned directory and run `makepkg -si` to compile and install the package.

#### Enable Gmail labels in the e-mail list (index_format):

In your **.muttrc** add this to the **index_format**: ` %?y?(%y)?`

Or, you can add this instead: `[%-15.15y]` to show brackets around the labels.

If the labels won't show up (or they won't get refreshed), make sure you disable the `header_cache` (do **NOT** `set header_cache`)





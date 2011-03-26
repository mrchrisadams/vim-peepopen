This isn't my plugin per se - I use [Janus][] flavoured [MacVim][] and [PeepOpen][] together, and
whenever I'd rebuild Vim, I'd always have to remember after upgrading to
open Peepopen independently of Vim, and then hit 'install MacVim
Plugin'.

When I found out that all Peepopen was doing was putting a plugin in
`.vim/plugins`, the simplest thing to do seems to be create a repo
somewhere, and pull in the Peepopen Plugin when running an upgrade, or
building it.

### How to use this 

Add the following line to your janus Rakefile, and it should be pulled
in when building Vim's plugins:

		vim_plugin_task "peepopen",         "git://github.com/mrchrisadams/vim-peepopen.git"

And PeepOpen should be available to you without having to explicitly click 'install plugin any more'

<!-- links-->
[MacVim]:   'http://code.google.com/p/macvim/'      
[Janus]:    'https://github.com/carlhuda/janus'     
[PeepOpen]: 'http://peepcode.com/products/peepopen' 

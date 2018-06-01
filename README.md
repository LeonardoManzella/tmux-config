## What is tmux?
The official verbiage describes tmux as a screen multiplexer, similar to GNU Screen. Essentially that means that tmux lets you tile window panes in a command-line environment. This in turn allows you to run, or keep an eye on, multiple programs within one terminal.

A common use-case for tmux is on a remote server where you have a common layout that you always use, and want a way to quickly jump into and out of. An example would be if you’re connecting through a jump server and have other remote SSH sessions you would like to be connected to simultaneously. Similarly, if you have to hop into Vim, you can use tmux to give you access to your shell or a REPL in the same terminal window for a IDE-like experience.

## Why bother customizing tmux?
tmux isn't just for running tasks in servers detached from a session.
It can also be a nice tool to have as a developer

## Terminal multiplexing can look good `>^.^<`
![](https://i.imgur.com/AA9qTDI.png)


## Installation
Copy the `.tmux.conf` file to your home: `~/`

Start a new tmux terminal with `tmux new`

Tap `Control + B` then `I` (yes, UPPERCASE) to install all the plugins via tpm plugin manager

Ready to go!  `>^.^<`


## Layout restoration
Courtesy of [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect), `Control + B Control + S` to save the current layout, 
`Control + B Control + R` to restore the last saved layout.
It can be configured to restore particular programs, for example, the provided config file restores vim and neovim, sourcing a `Session.vim` file if it exists.




## More human-friendly keybindings
Changing between panes in the same window is easier with vim-style keybindings

`Control + H` : go to pane to the left

`Control + J` : go to pane below

`Control + K` : go to pane above

`Control + L` : go to pane to the right

Seamless navigation with vim splits can be achieved with the plugin: [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)

Splitting panes has more reasonable keybindings (or at least are consistent with my `.i3/config` :D)

`Control + B  V`: vertical split.

`Control + B  ;`: horizontal split.

## TODO
* Different bar colors when running in a server, perhaps by reading an environment variable?

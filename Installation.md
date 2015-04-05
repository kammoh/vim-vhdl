#How to install the vim-vhdl plugin

To install the plugin,

  * copy vhdl.vim and vstp.vim in your ~/.vim/plugin/ directory (if it doesn't exist create it).

  * Modify template/vhdl file as you want.

  * Then in your ~/.vim/ftplugin/ directory make a file vhd.vim with calls to template function and plugin function:

```
call VHDL_init()
call VSTpl_ifnew('$your_template_directory$/vhdl')
```
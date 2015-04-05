# Introduction #

Designing component with VHDL language is very verbose. Then lot of declarations and connections can be done automatically with a great editor and his plugin. Unfortunately only Emacs has a good plugin to write VHDL code ... it's bad.

To correct this, the goal of vim-vhdl is to provide a better plugin than emacs-vhdl mode because nothing can be better than vim ;-)

# Details #

The main features of this plugin are :

**Done (but with bugs)** :

  * indent beautifully the code with ":" and "=>" aligned.
  * when component is instanced, automatically copy all signal interface loaded from the wright file.
  * Write a template (from ~/.template/vhdl when empty project is open), with author,date and filename as entity name.
  * write some cools abbreviations (from Andreas for example).

**To Do** :


  * When component is connected in architecture body copy all signals and let the user to modify if wanted :
a component declared as this
```
      component littlecomp
          port (
               clk : in std_logic;
               A   : in sld_logic;
               B   : in std_logic;
               C   : out std_logic
          );
```

in the architecture will be used in the architecture body when we map port
```
      con_littlecomp : littlecomp
       port map (
```
at this moment copy signal name like following :
```
      con_littlecomp : littlecomp
       port map (
                clk => clk,
                A   => A,
                B   => B,
                C   => C
                 );
```
The user will modify right signal if necessary.


# Link #

  * Some tips come from [Andreas Müller](http://www.forum-und-contact.ethz.ch/~andrmuel/vhdl-with-vim.html)
  * [vim](http://www.vim.org)
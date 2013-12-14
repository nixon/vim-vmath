# vmath.vim

Damian Conway's vmath plugin for vim as demonstrated at his OSCON 2013
"More Instantly Better Vim" presentation.  Calculates the sum, average,
min, and max for a visual region containing numbers.

# Installation

Copy vmath.vim to ~/.vim/plugin:

```bash
cp ./plugin/vmath.vim ~/.vim/plugin/
```

or use tpope's [pathogen](https://github.com/tpope/vim-pathogen):

```bash
cd ~/.vim/bundle
git clone git://github.com/nixon/vim-vmath.git
```

# Usage

Add the following key maps to ~/.vimrc:

```vim
vmap <expr>  ++  VMATH_YankAndAnalyse()
nmap         ++  vip++
```

Start vim, use visual mode to highlight a set of numbers, and use `++`.
The result will be output like:

```
sum: 21     avg: 3.5     min: 1     max: 6
```

The results are also stored in the following registers:

 * s : sum
 * a : average
 * n : min
 * x : max
 * r : range

which can then be pasted with `"sp`, etc.  The sum is also available in
the default yank buffer so it can be easily pasted with `p`.

# License

The original author placed vmath.vim in the public domain.

# References

 * http://www.oscon.com/oscon2013/public/schedule/detail/28875
 * https://docs.google.com/file/d/0Bx3f0gFZh5Jqc0MtcUstV3BKdTQ/edit
 * http://www.youtube.com/watch?v=aHm36-na4-4

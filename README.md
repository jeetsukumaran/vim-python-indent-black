
# vim-python-indent-black

This modifies the built-in Python `indentexpr` function to wrap the closing parenthesis, following the convention of [black](https://github.com/psf/black).

That is, this will autoindent the closing parenthesis so that it lines up with the starting column of the parent statement line:

```python
1: if (
2:     conditional1
3:     and conditional2
4:     ...
5:     and conditional3
6: ):
```

It also automatically sets the following values:

```
let g:pyindent_open_paren = 'shiftwidth()'
let g:pyindent_nested_paren = 'shiftwidth()'
let g:pyindent_continue = 'shiftwidth()'
let g:pyindent_close_paren = '-shiftwidth()'
```

If needed, you can get the default Vim autoindent settings by specifying the following:

```
let g:pyindent_open_paren = 'shiftwidth()*2'
let g:pyindent_nested_paren = 'shiftwidth()'
let g:pyindent_continue = 'shiftwidth()*2'
let g:pyindent_close_paren = '0'
```


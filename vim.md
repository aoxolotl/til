# Run commands based on filetype
You can run commands based on file type and map them to leaders. For example, on a `python` file.
```vim
"" Filetype specific commands
" Run python script
autocmd FileType python noremap <leader>y <Esc>:!clear; python %<CR>
```

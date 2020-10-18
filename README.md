# vimrc

"Basic highlight                                                                
syntax on                                                                       
                                                                                 
"Disable annoying beeping:                                                      
set noerrorbells                                                                
set vb t_vb=                                                                    
                                                                               
"To control the number of space characters that will be inserted when the tab key is pressed
set tabstop=4 softtabstop=4                                                     
set shiftwidth=4                                                                
set expandtab                                                                   
                                                                                
"Indention                                                                      
set autoindent                                                                  
set copyindent                                                                  
                                                                                
"Display line numbers                                                           
set nu                                                                          
                                                                                
"Spellcheck                                                                     
set spell spelllang=en_us                                                       
                                                                                
"Character encoding                                                             
set encoding=utf-8                                                              
set fileencoding=utf-8                                                          
                                                                                 
"Search                                                                         
set smartcase                                                                   
set incsearch                                                                   
                                                                              
set undodir=~/.vim/undodir                                                      
set undofile                                                                    
                                                                                
set colorcolumn=80                                                              
highlight ColorColumn ctermbg=0 guibg=lightgrey                                 
                                                                                
"vim-plug - Vim plugin manager                                                  
call plug#begin('~/.vim/plugged')                                               
                                                                                
Autocomplete, Flexible: configured like VSCode, extensions work like in        
"VSCode,                                                                        
 Plug 'neoclide/coc.nvim', {'branch':'release'}                                  
 
"Retro color scheme                                                             
Plug 'gruvbox-community/gruvbox'                                                
                                                                                
"Syntax highlighting                                                            
Plug 'sheerun/vim-polyglot'                                                     
                                                                                
"The plug-in visualizes undo history and makes it easier to browse and switch   
"between different undo branches. Not sure if it is that important?             
Plug 'mbbill/undotree'                                                          
                                                                                
call plug#end()                                                                 
                                                                                
" vim-prettier                                                                  
"let g:prettier#quickfix_enabled = 0                                            
"let g:prettier#quickfix_auto_focus = 0                                         
" prettier command for coc                                                      
command! -nargs=0 Prettier :CocCommand prettier.formatFile                      
" run prettier on save                                                          
"let g:prettier#autoformat = 0                                                  
"autocmd BufWritePre *.js,*.jsx,*.mjs,*.ts,*.tsx,*.css,*.less,*.scss,*.json,*.graphql,*.md,*.vue,*.yaml,*.html PrettierAsync
                                                                                
                                                                                
" coc configuration                                                             
let g:coc_global_extensions = [                                                 
            \ 'coc-pairs',                                                      
            \ 'coc-tsserver',                                                      
            \ 'coc-eslint',                                                     
            \ 'coc-prettier',                                                   
            \ 'coc-json',                                                       
            \]                                                                  
                                                                                 
colorscheme gruvbox                                                             
set background=dark      

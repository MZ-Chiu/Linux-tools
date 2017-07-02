#taglist
##下载
1）从http://www.vim.org/scripts/script.php?script_id=273下载安装包，也可以从http://vim-taglist.sourceforge.net/index.html下载。
##安装
2）进入~/.vim目录，将Taglist安装包解压，解压后会在~/.vim目录中生成几个新子目录，如plugin和doc（安装其它插件时，可能还会新建autoload等其它目录）。

3）进入~/.vim/doc目录，在Vim下运行"helptags ."命令。此步骤是将doc下的帮助文档加入到Vim的帮助主题中，这样我们就可以通过在Vim中运行“help taglist.txt”查看taglist帮助。
##使用
4）打开配置文件~/.vimrc，加入以下几行：
'''
" --The following support by taglist
let Tlist_Ctags_Cmd = '/usr/bin/ctags'
let Tlist_Auto_Open = 0
let Tlist_Show_One_File = 1		"Only show one tag list file in the same time
let Tlist_Exit_OnlyWindow = 1
let Tlist_Use_Right_Window = 0		"Tag list window positong
"let Tlist_WinHeight = 100
let Tlist_WinWidth = 40
"Tag list quick open key
noremap <F4> :TlistToggle<CR>		
"Updata ctags
noremap <F6> :!ctags -R<CR>		

'''

#supertab
##下载
http://www.vim.org/scripts/script.php?script_id=1643
##安装
用Vim打开.vba安装包文件。
在Vim命令行下运行命令“UseVimball ~/.vim”。此命令将安装包解压缩到~/.vim目录。VImball安装方式的便利之处在于你可以在任何目录打开.vba包安装，而不用切换到安装目的地目录。而且不用运行helptags命令安装帮助文档。
在~/.vimrc文件中加入以下这行：let g:SuperTabDefaultCompletionType="context" 

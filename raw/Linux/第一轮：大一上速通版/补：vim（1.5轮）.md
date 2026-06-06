## 1.
`hjkl:left down right up`
`q!:quit without saving` `wq:save and quit`
`x:delete a character` 
`i:type inserted` `a:insert in appending`
## 2.
`dw:delete word` 
`d$:delete to the end of a line`
`dd:delete a whole line`
`number motion:e.g.:2w`
`0:move to the start of the line`
`u:undo previous action`
`U:undo all the changes on a line`
`ctrl R:undo the undo's`
## 3.
`p:paste (used with dd/dw..)`
`r:replace`
`ce:retype this word till the end`
`c$:retype till the end of the line`
## 4.
`ctrl g:displays your path`
`G:moves to the end of the file`
`gg:moves to the first line`
`number G:moves to that line number`
`/word:search a word`
`/:search forward(down)`
`?:search backward(up)`
`n:to find the next occurence`
`N:to find in the opposite direction`
`ctrl o:to older position`
`ctrl i:to newer position`
`%:to find the match of (,[,{`
`:s/old/new:to substitue new for the first old in a line`
`:s/old/new/g:to substitue new for all old on a line`
`:%s/old/new/g:to substitue all occurrences in the file`
## 5.
`:! command:executes an external command`
`:w filename:writes the current vim file to disk with name filename`
`v motion :w filename:save the visually selected lines in filename`
`:r filename: read disk file filename and put it below the cursor`
`:r dir!:reads the output of the dir command and puts it below the cursor`
## 6.
`o:to open a line below the cursor`
`O:to open a line above the cursor`
`a:to insert text after the cursor`
`A:to insert text after the end of the line`
`e:move to the end of a word`
`y:copies text` `p:pastes it`
`R:enters replace mode until esc is pressed`
`:set ic:ignorecase` `:set is:incsearch`
`:set hls:hlsearch` `no :set command:switch off`
## 7.
`:help:open a help window`
`:help cmd:to find help on cmd`
`ctrl w:to jump to another window`
`:q:to close the help window`
`输入：开头的命令时 ctrl d 可查看该命令所有补全选项 tab补全`


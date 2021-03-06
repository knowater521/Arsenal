- `:`: 进入命令模式
- `esc`: 返回普通模式
- `Ctrl-o`: 进入衍生模式，比如插入模式下，`ctrl-o` 输入一个普通模式下的命令，执行完毕后，自动返回 插入模式。

# 光标移动

- `h,j,k,l`: 普通模式下，光标移动，左，下，上，右。（逆时针）
- `5h`: 重复执行5次h, 光标左移5位
- `0`: 行首
- `^`: 行首第一个非空白字符
- `$`: 行尾
- `g_`: 行尾最后一个非空白字符

- `w,e,b`: 普通模式下，光标以单词纬度移动。

- `W,E,B`: 同上，但是移动的单词可以包含标点。比如连字符`-`

- `Ctrl-d`, `Ctrl-u`: 半个屏幕向下，向上滚动。

- `Ctrl-B, Ctrl-F`: 滚动一个屏幕，通常会被我覆盖，我用来定义 emacs 光标移动方式。

- `zt,zz,zm`: 使当前行，处于屏幕的顶部，中间，底部。

- `H,M,L`: 光标定位到当前屏幕的，顶部，中间，底部。

- `gg`: 定位到文本开始处

- `G`: 定位到文本最后一行

- `5G`: 移动到第五行

- `:5`: 同上，移动到指定行

- `gd`: 找到当前变量定义处。

- `%`: 跳转匹配的括号, (,{,[,],},)

- `()`: back, forword

- `{}`: back,forword paragraph

- `[{`,`]}`: back, forword block

- `f{char},F{char}`: x是一个字符，向后跳到{char}字符出现的位置

- `t{char},T{char}`: x是一个字符，向前跳到{char}字符出现的位置

- `*`: 向后跳转到当前字符相同处, spacemacs 中无效

- `#`: 向前跳转到当前字符相同处，spacemacs 中无效

# 编辑模式

- `i`: 当前光标前插入
- `a`: 当前光标后插入
- `I`: 当前行首插入
- `A`: 当前行尾插入
- `o`: 当前行后插入
- `O`: 当前行前插入
- `wi`, `bi`, `ea`: 下一个单词前，单词后插入

- `r`: 重写当前一个字符

- `R`: 重写多个字符，需要手动退出

- `J`: 何必当前行和下一行

- `xp`: 交换当前和下一个字符位置

- `u`: undo

- `Ctrl+r`: redo

- `.`: repeat last command, 可用于 redo

# 复制，粘贴，裁切

- `x`: 删除当前光标字符
- `X`: 删除当前光标前字符
- `D`: 删除当前行后字符
- `C`: 重写当前行后字符，就是执行了 `D`， `a`
- `cc`: 重写当前行，相当于 `dd`, `i`
- `cw`: 重写当前词，相当于 `dw`, `i`
- `s`: 重写当前字符
- `S`: 相当于 `cc`
- `d`: 执行关于删除的引导键, 比如 `d0`, `d$`
- `dd`: 删除当前行
- `dw`: 向后删除当前词
- `db`: 向前删除当前词
- `ndw`: n表示重复执行

- `yy`: yank 就是拷贝的意思，拷贝当前行

- `yw`: 复制当前光标到当前词尾的字符

- `yb`: 复制当前光标到当前词首的字符

- `p`: 当前光标后粘贴

- `P`: 当前光标前粘贴

- `v`: 进入 visual 模式

- `V`: 进入visual 模式，选取单位位行

- `Ctrl+v`: 进入 visual 模式，选取单位为块

- `<`: 进入 visual 模式后， 向左进行 index

- `>`: 进入 visual 模式后， 向右进行 index

- `y`: 进入 visual 模式后，复制选中字符

- `x`: 进入 visual 模式后， 裁切选中字符

- `d`: 进入 visual 模式后，删除选中字符， 效果同上

- `~`: 进入 visual 模式后，将选中字符大小写交换

# ctrl 组合按键

- `ctrl-r`: redo (可被系统 Replace 替换)， 在 vim 中 使用 `.` 进行 redo
- `ctrl-d`: 向下翻滚半个屏幕
- `ctrl-u`: 向上翻滚半个屏幕·
- `ctrl-i`: jump to your previous navigation location
- `ctrl-o`: jump back to where you where
- `ctrl-e`: scroll up one line (可被系统 光标移动到行末替换)
- `ctrl-y`: scroll down one line, 屏幕向上移动一行
- `ctrl-v`: 竖向选择 virsual模式， （可被系统粘贴替换）
- `ctrl-f`: 整屏向下移动，（可被系统光标向前移动替换）
- `ctrl-b`: 整屏向上移动， （可被系统光标向后移动替换）
- `ctrl-w {char}`: 针对多窗口 操作的触发按键
- `ctrl-w c`: close tab
- `ctrl-w q`: quite a window
- `ctrl-w s`: 水平分割窗口
- `ctrl-w v`: 垂直分割窗口
- `ctrl-w w`: 在不同 window 直接切换
- `ctrl-w p`: 返回上一次聚焦的 window
- `ctrl-w h/j/k/l`: 移动光标聚焦在上下左右窗口

# 搜索
- 设置搜索结果高亮: `set hlsearch!`
- 取消高亮设置: `noh`

# 小技巧

- 插入3个 go, 可使用 `3i go {esc}`

- 查找当前光标后，第三个s, 可使用 `3fs`

- `zc`, `zo`: 代码折行收起，展开

- `J`: 合并两行

- `>`: 控制缩进

- `gt`: 移动到下一个 tab 页

- `gT`: 移动到上一个 tab 页


## 参考资料
- 返回 normal, 推荐使用 `ctrl-[` , 避免过多的自定义
- 减少使用 `hjkl` 移动光标，[habit-breaking-habit-making](http://vimcasts.org/blog/2013/02/habit-breaking-habit-making/)

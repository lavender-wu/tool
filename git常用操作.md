- 合并多条commit

  ```
  1.合并commit
    1）编辑最近number条commit
  	 git rebase -i HEAD~number
    2）编辑到版本号为3a4226b的之前的commit（注意不包含3a4226b）
       git rebase -i 3a4226b
  // 终端会进入编辑状态，此时按键盘 i 之后才能通过键盘来输入你的修改信息
  2.输入 i
  3.最上方（即最初一条）commit 不变，将下面合并的commit 前面的pick 该为s
  4.输入esc 保存修改
  5.shift + : + wq! 退出编辑状态
  // 此时 终端会打开一个编辑状态，给你去修改合并后commit的内容（即使前面有改了也是不生效）
  6. 1）需要修改则输入 i 进入编辑状态，修改commit内容后 保存并退出（命令同上）
     2）若不需要修改，保存并退出即可
  7.可以git log 查看提交记录，可以发现已经被合并，但本地仍然保留之前的commit，提交到远程只有合并的commit
  ```

  


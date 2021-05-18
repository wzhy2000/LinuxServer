# 用户

## 增加
`useradd username [-g]` : username填入你的用户名  
`-g` 指定用户组

## 删除
`userdel [-r] username`
建议连带参数`-r`使用，删除用户主目录  
`-r` 删除用户主目录

## 查看列表
`cat /etc/passwd`  
更精细的用户列表：`cat /etc/passwd | grep -v nologin | grep -v halt | grep -v shutdown|awk -F":" '{ print $1"|"$3"|"$4 }'|more`  
当前活跃用户：`w`

# 用户组

## 增加
`groupadd groupname`

## 修改用户的用户组
`usermod -g groupname username`

## 删除
`groupdel [-r] groupname`  
`-r`: 级联删除

## 查看列表
`cat /etc/group`
# 文件操作加强

### 文件备份



```python
    # 任意文件添加 备份 样式
    old_file_name = input('请输入您要备份的文件: ')

    index = old_file_name.rfind('.')

    if index > 0:                              # 后缀下标是大于 0 的
    postfix = old_file_name[index:]

    new_file_name = old_file_name[:index] + '[备份]' + postfix

    old_file = open(old_file_name)
    new_file = open(new_file_name, 'w')

    while True:
        con = old_file.read(1024)
        if len(con) == 0:
            break
        new_file.write(con)

    old_file.close()
    new_file.close()
```




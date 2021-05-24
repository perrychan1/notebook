# tar

```bash
# .tag.gz
tar -xvf myfile.tag.gz

# 打包当前文件夹下的全部文件，但不包含当前文件夹
cd dir/ && tar -czvf ../archive.tar.gz . && cd -
# or
tar -czvf archive.tar.gz -C dir .
# The -C dir tells tar to change the current directory to my_directory, and then . means "add the entire current directory" (including hidden files and sub-directories).

zip [options] zipfile files_list

# zip file.js:
zip archive.zip file.js

# zip a directory recursively:
zip -r archive.zip directory

unzip myfile.zip
```


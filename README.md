# cdr-package
custom construction

7za.exe
最常用的命令有a（压缩）、x（解压）

压缩文件 zip
7za.exe a -tzip temp.zip file1.txt file2.txt folder/
a 是7za.exe工具的选项，表示执行添加（压缩）操作。
-tzip 是7za.exe工具的选项，用于指定压缩格式为ZIP。
archive.zip 是要创建的ZIP存档文件的名称。
file1.txt、file2.txt 是要包含在ZIP存档中的文件。
folder/ 是要包含在ZIP存档中的目录。

7za.exe x -y xxx.zip
-y 使 7-Zip 执行命令时的大多数提示失效。您可以使用此选项来阻止在 e (释放) 和 x (完整路径释放) 命令中文件覆盖时的提示。
总结： -y 是覆盖，用于指定在解压缩时不询问任何问题，即自动确认所有提示。


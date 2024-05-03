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

7z格式
7z XZ BZIP2 GZIP TAR zip
仅解压
ARJ CAB CHM CPIO DEB DMG FAT HFS ISO LZH LZMA MBR MSI NSIS RAR RPM UDF VHDWIM XAR Z

添加压缩包
7z a package.7z .\product\* -r -mx=9
a：
表示add命令，即新建一个压缩文件，该压缩文件存放在当前目录下
-r：
表示遍历所有的子目录，每个文件都执行压缩操作，添加到压缩文件中。
-mx：
表示压缩等级，9级是最高等级。默认等级是5。

a：
表示add命令，即新建一个压缩文件，该压缩文件存放在当前目录下
-r：
表示遍历所有的子目录，每个文件都执行压缩操作，添加到压缩文件中。
-mx：
表示压缩等级，9级是最高等级。默认等级是5。

3、从压缩包删除文件
7z package.7z*.back -r

4、释放文件

7z x package.7z -o.\mydir -aoa
释放package.7z文件到当前mydir文件夹

x：
表示解压缩，并且使得压缩包内的文件所在的目录结构保持不变。
如果希望解压缩后所有的文件都存放在同一个目录下，则使用 e 这个命令。
-o.\mydir
表示把压缩包内的文件解压缩到 .\mydir 目录下。-o 这个参数用于指定输出目录。
-aoa：
表示直接覆盖现有文件，而没有任何提示
类似其他参数：
-aos：跳过现有文件，其不会被覆盖。
-aou：如果相同文件名的文件以存在，将自动重命名被释放的文件。Eg：文件 file.txt 将被自动重命名为 file_1.txt。
-aot：如果相同文件名的文件以存在，将自动重命名现有的文件。Eg：文件 file.txt 将被自动重命名为 file_1.txt。

5、使用密码进行压缩与解压缩

7z a package-p.7z .\product\* -r -mx=9 -psecret
对.\product\下的文件进行压缩，解压时需要使用密码secret

7z x package-p.7z -o.\mydir -aoa -psecret
使用密码secret对package-p.7z进行解压




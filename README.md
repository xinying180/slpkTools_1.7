# slpkTools_1.7
slpk相关工具，针对i3s 1.7版本
如果Pro中直接执行Create Integrated Mesh Scene Layer Package工具报错，可以先使用Check osgb files工具，然后再使用osgbToslpk工具。
Check osgb files工具：
1，输入osgb文件夹路径到Data文件夹
2，工具会将有问题的osgb数据剪切到同名的Data0目录下，并且生成errorOSGBFiles.txt文本文件，记录下本次执行过程中有问题的osgb数据路径

osgbToslpk工具：
1，输入osgb文件夹路径那里选择Data的上一级文件夹；
2，工具会自动寻找输入文件夹下有没有metadata.xml文件，如果有的话，输入锚点文件参数下会自动识别出该文件，
没有的话可以手动选择shapefile文件；
3，空间参考输入WKID即可。

如果需要优化slpk的大小，可以使用Optimize Slpk Size工具，可以优化3D Object以及倾斜类型的slpk。
Optimize Slpk Size工具：
1，输入slpk所在的文件夹路径即可，支持批量执行
2，输出的slpk在同一文件夹下，以原始slpk名称+_tar结尾命名。

tips: 
1，以上工具针对Pro 2.5以及I3S 1.7版本
2，如果需要使用osgbToslpk工具，则不要删除目录下的OSG文件夹

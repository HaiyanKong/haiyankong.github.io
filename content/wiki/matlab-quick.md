---
title: "MATLAB 速查"
slug: "matlab-quick"
toc: true
tocBorder: true
---

> 本文内容：MATLAB 速查

# 画图

```matlab
% ≥ MATLAB 2018b

%% 给图形窗口添加一个总标题
sgtitle('Title');

%% 打开旧版本 MATLAB 画的图
open('path\\picture.fig');
```

# 清理

```matlab
close % 清除 workspace

clc % 清除 command Windows

close all %关闭所有图片

keep = {'hdr', 'data'};
clearvars('-except', keep{:}); % 保留变量 hdr 和 data，其余清除

clearvars -except hdr data % 保留变量 hdr 和 data，其余清除
```

# 存储

```matlab
save('D:\\\\appendix\\\\data.mat', ‘variables’);
% D:\\\\appendix\\\\data.mat 存储路径
% variables 要存储的变量

save('D:\\\\appendix\\\\data.mat');
% 存储 workspace 的所有变量
```

# 拼接

```matlab
%% 1.  `fullfile` 函数
% 专门用于拼接文件路径的函数，会自动根据操作系统选择正确的路径分隔符
folder = 'C:\Users\Username\Documents';
filename = 'data.txt';
fullpath = fullfile(folder, filename); % C:\Users\Username\Documents\data.txt


%% 2. `strcat` 函数
% 用于拼接字符串，并且会去除尾部空格，但不自动处理路径分隔符
str1 = 'Hello ';
str2 = 'World';
result = strcat(str1, str2); % HelloWorld


%% 3. 方括号 `[ ]` 
% 直接将字符串连接在一起，但不会自动去除空格，也不会像 fullfile 自动处理路径分隔符
folder = 'C:\Users\Username\Documents';
filename = 'data.txt';
fullpath = [folder, '\', filename]; % C:\Users\Username\Documents\data.txt


%% 4. `sprintf` 函数
% 用于格式化字符串，并将结果作为返回值，可以控制输出的格式（例如小数点位数、对齐、填充等）
x = 3.14159;
str1 = [ 'Value of x: ', num2str(x) ];  % Value of x: 3.14159
str2 = sprintf('Value of x: %.2f', x);  % Value of x: 3.14


%% 5. `join` 函数
% 用于连接字符串数组或单元格数组，可以方便地插入分隔符，并且是处理多个字符串时的推荐方法
strArray = ["apple", "banana", "cherry"];
result = join(strArray, " | "); % apple | banana | cherry

strArray = ["apple", "banana", "cherry"];
result = join(strArray); % applebananacherry
```

# 查看变量类型

```matlab
class(variables) % ‘variables’ 要查看的变量
```

# 寻找函数位置

```matlab
which getAppDir  % 寻找 getAppDir 位置
```

# 写 function

```matlab
function [ c ] = qpfh( a,b )
	c = a^2 + b^2;
end

% 来求两个数的平方和
```

# 教程

MATLAB_for_Brain_and_Cognitive_Scientists_2017_The-MIT-Press

# 杂项

## MATLAB warning: saving variables to older MAT-file versions

This blog will present a solution to address the MATLAB warning: Variable cannot be saved to a MAT-file with a version older than 7.3.

When using MATLAB to save variables, you might encounter a warning message similar to the one below:

```
Warning: The variable 'a' cannot be saved to a MAT-file with a version
older than 7.3.
```

To resolve this issue, you can follow these steps:

- Open MATLAB and click on Preferences.
- Navigate to the General tab and select MAT-Files.
- Choose the first option: "MATLAB Version 7.3 or later (save -v7.3)."

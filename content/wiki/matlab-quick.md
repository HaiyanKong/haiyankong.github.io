---
title: "MATLAB 速查"
slug: "matlab-quick"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

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
%% 1. 使用方括号 `[ ]` 进行拼接

% 这种方式简单直接，适用于连接少量字符串

str1 = 'Hello';
str2 = 'World';
combined_str = [str1, str2];  % 结果为 'HelloWorld'

path = ['D:/appendix/data/', subj{i},'/',run{i},'.ds'];

%% 2. 使用 `strcat` 函数

% `strcat` 函数可以接受多个输入参数，并按顺序连接它们
% 注意，`strcat` 在处理字符数组时需要注意维度匹配问题

str1 = 'Hello';
str2 = 'World';
combined_str = strcat(str1, str2);  % 结果为 'HelloWorld'

path = strcat('D:/appendix/data/', subj{i},'/',run{i},'.ds');

%% 3. 使用 `sprintf` 函数

% `sprintf` 可以像C语言的 `printf` 一样格式化输出，也可以用来拼接字符串
% 这种方式可以更灵活地控制输出格式，但相对于简单拼接来说稍显复杂

str1 = 'Hello';
str2 = 'World';
combined_str = sprintf('%s%s', str1, str2);  % 结果为 'HelloWorld'

path = sprintf('D:/appendix/data/%s/%s.ds', subj{i},run{i});

%% 4. 使用字符串数组

% 如果有多个字符串需要拼接，可以使用字符串数组进行操作
% 这种方法适合需要处理多行文本的情况

str1 = 'Hello';
str2 = 'World';
str_array = [str1; str2];  % 创建字符串数组
combined_str = strjoin(str_array);  % 默认按行拼接，结果为 'HelloWorld'

%% 5. 使用 `join` 函数

% `join` 函数可以用指定的分隔符将字符串数组或单元数组连接起来
% 可以通过指定分隔符参数来进行自定义拼接

str1 = 'Hello';
str2 = 'World';
str_array = {str1, str2};  % 创建单元数组
combined_str = join(str_array);  % 默认使用空格拼接，结果为 'Hello World'
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

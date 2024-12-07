---
title: "MATLAB 笔记"
slug: "matlan-note"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

> 本文内容：MATLAB 笔记

# 各种乱七八糟还没整理的东西

## 20211107

```matlab
%%  MATLAB 学习笔记 20211107

% MATLAB 简介
% 特点
    % 区分大小写
    % 优先列的语言——数据提取
% 注意事项
    % set path——default（e.g., SPM 和 EEGlab 会冲突);
    % 当前路径——数据所在的路径
% 格式
    % *.m “代码文件”;
    % *.mat/.txt "数据文件"

%%  常用命令(该行命令结果不在命令窗口中显示)
clear                                              % 清除工作空间中的所有变量
clear x                                              % 清除工作空间中的变量x
clc                                                                  % 清屏
help                                                                 % 帮助
pwd                                                           % 当前工作路径
who                                                   % 查看工作空间中的变量
whos                                           % 查看工作空间中变量的详细信息

%%  数学运算
1+1; 2-1; 2*1; 1/2;                                               % 四则运算
2^3;                                                                 % n次幂
x=16; sqrt(x); x^(1/2);                                         % x 的平方根
exp(x)                                                    % 自然对数e的x次幂
log(x)                                            % 以自然对数e为底的对数函数
log10(x)                                                % 以10为底的对数函数
abs(x)                                                         % 求x的绝对值
mod(x,n)                                           % x除以n的余数 mod(9,2)=1
round(x)                                          % 对x四舍五入 round(1.6)=2
fix(x)                                % 去掉x的小数部分，即向0取整 fix(1.6)=1
ceil(x)                                     % 向正无穷取最小整数 ceil(1.6)=2
floor(x)                                   % 向负无穷取最大整数 floor(1.6)=1

pi                                                                % 圆周率π
sin(x)                          % 正弦，sin(x)的参数为弧度，sind(x)参数为角度
sind(x)                                             % sin(x)=sind(x/pi*180)
asin(x)
asind(x)                                    % 反正弦，即已知正弦值求弧度/角度
cos(x)                                                               % 余弦
acos(x)                                                             % 反余弦
tan(x)                                              % 正切，即sinx(x)/cos(x)
atan(x)                                                            % 反正切

%% 基本数据结构
% 数字
    6;
% 字符串 ' '
    'hello';
% 数组  [ ]
    [1 2 3 4]; % 一维数组
    [12 13 14 15;16 17 18 19]; % 二维数组
    % 三维数组
    [10:20:110] % 使用步长的方式定义数组,步长定义的数组可以不加[]
    a=[x1:n:x2];	% 以x1开始，n为步长，到x2为止的数列
    % 例：a=[2:3:8]; 得到a=[2 5 8]; a=[7:-2:-1]; 得到a=[7 5 3 1 -1];
    % 若结束值不等于起始值加n步长，则结束值为起始值加(n-1)步长
    % 例：a=[1:2:6]; 得到a=[1 3 5];
% 胞元 { }
    {'zhang',3,'wang'};
 % 结构体
    NIRS.fs = 2.44;
    NIRS.wavelength = [760, 830];
    NIRS.oxydata = [65,70,89,99];

%%  特殊数组
ones(4,5)
% 生成 4*5 的矩阵数组，矩阵各元素均为 1
zeros(4,5)
% 生成 4*5 的矩阵数组，矩阵各元素均为 0
eye(4,5)
% 生成 4*5 的矩阵数组，其中对角线元素为 1，其余元素为 0
magic(5)
% 生成 5*5 的矩阵数组，由1到5^2组成，且各行、各列、对角线的和均相同
repmat(x,m,n)
% 把矩阵数组x复制m行n列；
% 如x=[1 2; 3 4]; repmat(x,2,3)=[1 2 1 2; 3 4 3 4; 1 2 1 2; 3 4 3 4];

%%  矩阵/向量运算
a(n); % 取出矩阵数组a中第n个元素
a(end); % 取出矩阵a中最后一个元素
a(end-1) % 取出矩阵a中倒数第二个元素
a(m,n) % 取出矩阵a中第m行第n列的元素
% 如a=[1 3 7; 2 9 5; 4 8 6],则a([1 2],[2 3])=[3 7; 9 5];
% 即取第1、2行的第2、3列的元素
a(m,:); % 取出矩阵第m行所有元素
a(:,n); % 取出矩阵第n列所有元素

a(m,n)=x;
% 将矩阵a中第m行第n列的元素赋值x；
% 若m/n超出矩阵行/列，则补充其余值为0
% 如a=[1 3 7; 2 9 5; 4 8 6]; a(1,2)=2; 得到a=[1 2 7; 2 9 5; 4 8 6];
% 特别地，对于向量a，若a(n)=[]，则删除第n个元素
% 如a=[1:2:5]; a(2)=[]; a=[1 5];

a';
% 将矩阵a转置

a(:);
% 将矩阵a的元素按列堆叠，产生一个新的列向量。
% 如a=[1 3 7; 2 9 5; 4 8 6];则a(:)=[1 2 4 3 9 8 7 5 6]’;

reshape(a,m,n)
% 将矩阵a按列重排后，转换成m行n列的新矩阵
% 如 a=[1 2 3 4; 5 6 7 8];
% 则 reshape(a,4,2)=[1 3; 5 7; 2 4; 6 8];

[m,n]=size(a);
% 返回矩阵的行数m和列数n
length(a);
% 返回矩阵或向量的行列数中较大值
max(a);
% 返回矩阵a中每一列的最大值
min(a)
% 返回矩阵a中每一列的最小值

a=[1 2 2 3];
b=[2 3 4 5];
c=[1 2;0 3];
isequal(a,b)
% 判断向量或矩阵a和b是否相同；相同，值为1；不同，值为0.
find(c);
%找到矩阵a中所有不为零的数，返回其位置

%% 数据的提取

% 数组[]形成，()提取

a1 = [1 3 5 7 9 11 13];
% 一维数组
a1(n);
% 从a1数组中提取第n个位置的数据
% 从a1数组中同时提取多个位置的数据
a1([m,n]);
% 从a1数组中提取第m个位置的数据和第n个位置的数据
a1(m:n);
% 从a1数组中提取第m个位置到第n个位置的数据
a1(m:end);
% 从a1数组中提取第m个位置到最后一个位置的数据
a1(m:end-1);
% 从a1数组中提取第m个位置到倒数第二个位置的数据
% 步长的方式不支持该方法，提取时支持该方法
a1(:);
% 数组a1中的数据全部提取出来
% matlab是一种优先列的语言，因此提取的时候列优先
a1(:)';
% 若要转换为行，则使用'转置

school1 = [91 92 93 94; 95 96 97 98; 99 90 91 92];
% 二维数组
school1(n,m);
% 从数组school1中提取第n行第m列的数据
school1(n,[m,l]);
% 从数组school1中提取第n行第m列和第l列的数据
school1(:,3)
% 从数组school1中提取第3列的数据
school1(2,:)
% 从数组school1中提取第二行的数据
school1(2:end,2:end);
% 从数组school1中提取第二到最后一行、从第二到最后一列的数据
score(2,[2:3],[2:4])

% 胞元用{}生成，用{}提取

% 结构体的提取
subj(2,2).name

%% 数据的修改
% 修改对应于提取
a2 = [1 2 3 4;5 6 7 8];
a2([4,5]) = [666 333];% 不要忘记matlab列优先
school3 = [1 5 9 13;2 6 10 14;3 7 11 15;4 8 12 16];
school3([2,3],[2,4]) = [66,144; 77,155]

%%  随机与排序
rand(m,n)
% 生成m行n列在0到1间均匀分布的随机数
randn(m,n)
% 生成m行n列以0为均值，1为方差的随机数
randi(x,m,n)
% 生成m行n列的矩阵，其中元素为1到x之间的随机整数
randperm(n)
% 生成1至n随机排列的行向量
shuffle(x)
% 将行向量x的各元素随机排列
% 注：某些版本的shuffle命令可以支持对矩阵按行或列进行随机排列
% 详情可以help shuffle查看
sort(x)
% 对于向量x，将x中的元素按升序排列
sort(x,DIM,mode)
% 对于矩阵x，将x中的元素按指定维度按指定顺序排列，
% 其中DIM=1为按列排序，DIM=2为按行排序；
mode='ascend';
% 升序
mode='descend';
% 降序
% 如对于x=[3 7 5; 0 4 2];
% 则sort(x,1,'ascend')=[0 4 2; 3 7 5];
% sort(x,2,'descend')=[7 5 3; 4 2 0];

%% 统计运算
mean(x,DIM)
% 计算矩阵x每列（DIM=1）或每行（DIM=2）的平均值，
% 如对于x=[3 7 5; 0 4 2; 2 9 7];
% 则mean(x,1)=[1.667 6.667 4.667]，mean(x,2)=[5; 2; 6]；
% 如需计算某些元素的均值，可首先取出该元素，然后将其按列堆叠，再求均值，
% 如z=x(:,2:3); mean(z(:))，则可求矩阵x中第二列和第三列元素的均值
median(x)
% 计算矩阵x每一列的中位数
sum(x)
% 计算矩阵x每一列的和
std(x)
% 计算行向量x的方差，若x为矩阵，计算每列的方差

%%  逻辑判断
a==b;
% 判断a的值是否与b相等，如果a为矩阵，b为常数
% 则a中各个元素与b进行比较；
% 若a、b均为矩阵，则a、b行列数必须相等，分别判断相对应的元素是否相等
% 相等返回1（true），不等返回0（false）
% 注意，逻辑判断为双等号，区别于赋值单等号
a>b;
% 判断a的值是否大于b
a>=b;
% 判断a的值是否不小于b
a<b;
% 判断a的值是否小于b
a<=b;
% 判断a的值是否不大于b
a~=b;
% 判断a的值是否与b不等
&
% 逻辑与
|
% 逻辑或

% 比较
a=[0 0 2 1];
b=[3 0 2 0];
a==b;
% 返回[0 1 1 0] (逐个元素比较是否相等)
a~=b;
% 返回[1 0 0 1] (逐个元素比较是否不等)
a&b;
% 返回[0 0 1 0] (各非零元素均看作1，只有同时为真a&b才为真）
a|b;
% 返回[1 0 1 1] (各非零元素均看作1，有一为真a|b即为真）
```

## 20220625

```matlab
%%  20220625
clear;clc;

%%
a = 1
b = '1'
c = 'A'
class(a)
b_1 = class(b)
c_1 = class(c)
d = [1 3]
e = [1,3,5,8,9,10]
f = [3;5]
g = [1,3,5,8,9,10;1,2,3,4,5,6]
h = f'
i = 1:1:100
j = 100:-1:1
k = length(e)                                           % 查看一维向量的元素

%%
clear
clc

l = [2,6,1,9,4,8,3]
l_1 = class(l)                                                   % 查看类型
l_2 = length(l)                                              % 查看元素个数
l(4) = 19
l([2,5]) = [16,14]                                        % 提取更改多个原始
m = l(end)
l([end-3:end]) = [1,2,3,4]                                % 提取更改后四个数
l(end-3:end) = [1,2,3,4]                                  % 提取更改后四个数
l(3) = []                                                   % 删除某一个元素
n = [1,2]
n(3) = l(1)
n(4:7) = l(1:4)

%%
clear;clc;

o = [1:3]
p = [4:6]
q = [o;p]
r = q'
s(4,5) = 1
t = rand (4,5)
u = t(2,2:4)
v = t(:,2)

%%
clear;clc;

x = size(t)
x_1 = size(t,1)
x_2 = size(t,2)

%%
clear;clc;

y = ['hello','world']
z = ['hello';'world']

%%
clear;clc;

A{1,1} = 1
A{1,2} = 1:10
A{2,1} = 'sub001.mat'
%A{2,2} = []
A{1,1} = 'hello world'
class(A)

B = rand(3,4)

%%
clear;clc;

Student.age = 18                                               % 维度1
Student.name = 'xiao'                                          % 维度2
Student.scores = rand(10,1)                                    % 维度3
Student.scores                                                 % 读取结构体
class(Student)

%% 保存与导入

% way1：右击可以保存
% way2：下面代码
save('student.mat','Student')
save('D:\\\\kdat\\\\day2\\\\student.mat','Student')

% way1：直接拖进来
% way2：下面代码
load('student.mat')
load('D:\\\\kdat\\\\day2\\\\student.mat')

%% 练习
clear
clc
load('D:\\\\kdat\\\\day2\\\\sub001.mat');
% load('D:\\\\kdat\\\\day2\\\\sub002.mat')

% 20点51卡了

% fs是采样率
% nch是通道数
% 查看大小
size(nirs_data.oxyData);
dc(:,:,1) = nirs_data.oxyData;
dc(:,:,2) = nirs_data.dxyData;
dc(:,:,3) = nirs_data.tHbData;
roi = dc([100:150,end-499:end],:,1:2);

%%
qpfh(3,4)
doc qpfh

%%
C = 7
D = num2str(C)
% 将数字转换成字符串
E = ['sub00',1,'.mat']
F = ['sub00',num2str(1),'.mat']

% strcat 拼接字符串
    % [] 也可以拼接字符串
G = strcat('sub00',num2str(1),'.mat')

%% for循环
H = 10
if I > 10
    I = I+1
end

H =10
if I == 10
    I = I+1
end

H = 10
if H > 10
    H = H+1;
else
    H = H*10;
end

% 卡了
H = 10
if H > 11
    H = H+1;
elseif H > 10
    H = H +10;
else H = H*5;
end

disp(H)

%%
for J = 1:10;
    K = J*J;
    disp(K)
end

for J = [1,2,3,4,5]
    J
end

%%
% 假如有30个被试
% 文件名分别是
% sub001.mat to sub030.mat
% 写段代码一次打印出来每一个被试的文件名的信息

for i = 1:30;
    j = num2str(i);
    if i < 10
        name = strcat('sub00',j,'.mat');
    else
        name = strcat('sub0',j,'.mat');
    end
    disp(name)
end

% 21：49卡了

% 从sub001.mat拼接到sub100.mat
for i = 1:100;
    j = num2str(i);
    if i < 10
        name = strcat('sub00',j,'.mat');
    elseif i < 100
        name = strcat('sub0',j,'.mat');
    else
        name = strcat('sub',j,'.mat');
    end
    disp(name)
end
```

## 20220622

```matlab
%%
clear
clc

%%
clear
clc

a = 1
b = '1'
c = 'A'
class(a)
b_1 = class(b)
c_1 = class(c)
d = [1 3]
e = [1,3,5,8,9,10]
f = [3;5]
g = [1,3,5,8,9,10;1,2,3,4,5,6]
h = f'
i = 1:1:100
j = 100:-1:1
k = length(e)                                           % 查看一维向量的元素

%%
clear
clc

l = [2,6,1,9,4,8,3]
l_1 = class(l)                                                   % 查看类型
l_2 = length(l)                                              % 查看元素个数
l(4) = 19
l([2,5]) = [16,14]                                        % 提取更改多个原始
m = l(end)
l([end-3:end]) = [1,2,3,4]                                % 提取更改后四个数
l(end-3:end) = [1,2,3,4]                                  % 提取更改后四个数
l(3) = []                                                   % 删除某一个元素
n = [1,2]
n(3) = l(1)
n(4:7) = l(1:4)

%%
clear
clc

o = [1:3]
p = [4:6]
q = [o;p]
r = q'
s(4,5) = 1
t = rand (4,5)
u = t(2,2:4)
v = t(:,2)

%%
clear
clc

x = size(t)
x_1 = size(t,1)
x_2 = size(t,2)

%%
clear
clc

y = ['hello','world']
z = ['hello';'world']

%%
clear
clc

A{1,1} = 1
A{1,2} = 1:10
A{2,1} = 'sub001.mat'
%A{2,2} = []
A{1,1} = 'hello world'
class(A)

B = rand(3,4)

%%
clear
clc

Student.age = 18                                               % 维度1
Student.name = 'xiao'                                          % 维度2
Student.scores = rand(10,1)                                    % 维度3
Student.scores                                                 % 读取结构体
class(Student)

%% 保存与导入

% way1：右击可以保存
% way2：下面代码
save('student.mat','Student')
save('D:\\\\kdat\\\\day2\\\\student.mat','Student')

% way1：直接拖进来
% way2：下面代码
load('student.mat')
load('D:\\\\kdat\\\\day2\\\\student.mat')

%% 练习
clear
clc
load('D:\\\\kdat\\\\day2\\\\sub001.mat');
% load('D:\\\\kdat\\\\day2\\\\sub002.mat')

% 20点51卡了

% fs是采样率
% nch是通道数
% 查看大小
size(nirs_data.oxyData);
dc(:,:,1) = nirs_data.oxyData;
dc(:,:,2) = nirs_data.dxyData;
dc(:,:,3) = nirs_data.tHbData;
roi = dc([100:150,end-499:end],:,1:2);

%%
qpfh(3,4)
doc qpfh

%%
C = 7
D = num2str(C)
% 将数字转换成字符串
E = ['sub00',1,'.mat']
F = ['sub00',num2str(1),'.mat']

% strcat 拼接字符串
    % [] 也可以拼接字符串
G = strcat('sub00',num2str(1),'.mat')

%% for循环
H = 10
if I > 10
    I = I+1
end

H =10
if I == 10
    I = I+1
end

H = 10
if H > 10
    H = H+1;
else
    H = H*10;
end

% 卡了
H = 10
if H > 11
    H = H+1;
elseif H > 10
    H = H +10;
else H = H*5;
end

disp(H)

%%
for J = 1:10;
    K = J*J;
    disp(K)
end

for J = [1,2,3,4,5]
    J
end

%%
% 假如有30个被试
% 文件名分别是
% sub001.mat to sub030.mat
% 写段代码一次打印出来每一个被试的文件名的信息

for i = 1:30;
    j = num2str(i);
    if i < 10
        name = strcat('sub00',j,'.mat');
    else
        name = strcat('sub0',j,'.mat');
    end
    disp(name)
end

% 21：49卡了

% 从sub001.mat拼接到sub100.mat
for i = 1:100;
    j = num2str(i);
    if i < 10
        name = strcat('sub00',j,'.mat');
    elseif i < 100
        name = strcat('sub0',j,'.mat');
    else
        name = strcat('sub',j,'.mat');
    end
    disp(name)
end
```

## matlab_exercise_20220622

```matlab
%num2str 将数字转换成字符串
%strcat 拼接字符串的 - []
strcat('sub00',num2str(1),'.mat')
['sub00',num2str(1),'.mat']
a = 10
if a == 10
    a = a + 1;
end
a = 10
if a >10
    a = a + 1;
else
    a = a*10;
end

a = 10
if a > 11
    a = a + 1;
elseif a > 10
    a = a +2;
else
    a = a * 10;
end

for i = 1:10;
    b = i * i;
    disp(b)
end

for i = [2 5 9 10 13]
    i
end
% 假如我有一批被试 30个
%被试的文件名分别为
%sub01.mat sub02.mat . sub10.mat .. sub30.mat
%要求大家写段代码 依次打印每个被试的文件名的信息
% if for []/strcat disp
for i = 1:30;
    if i < 10;
        filename = ['sub0',num2str(i),'.mat'];
    else
        filename = ['sub',num2str(i),'.mat'];
    end
    disp(filename)
end

% 假如问我有100个被试 从sub001.mat拼接到sub100.mat
for i = 1:100;
    if i < 10;
        filename = ['sub00',num2str(i),'.mat'];
    elseif i < 100;
        filename = ['sub0',num2str(i),'.mat'];
    else
        filename = ['sub',num2str(i),'.mat'];
    end
    disp(filename)
end
```

## timeSelect

```matlab
clear;clc
filedir = 'D:\\\\datapath\\\\subject01';
filelist = dir(fullfile(filedir, '*.mat'));

for i = 1:numel(filelist)
    filename = filelist(i).name;
    T_indices = strfind(filename, 'T');
    last_T_index = T_indices(end);
    time = str2double(filename(last_T_index+1:last_T_index+6));
    filelist(i).time = time;
end

clearvars -except filelist
time_lower = 123000;
time_upper = 133000;
filtered_filelist = filelist([filelist.time] >= time_lower & [filelist.time] <= time_upper);
```

## findNaN

```matlab
nan_positions = {};

for i = 1:size(statdatas_HG.seens, 1)
    for j = 1:size(statdatas_HG.seens, 2)
        nan_positions{end+1} = find(isnan(statdatas_HG.seens{i, j}));
    end
end

nan_positions = cell2mat(nan_positions);
sum(isnan(imgTypes(1,:)))
```

## randomData

```matlab
clear;clc
for i=1:10
    a=randi([1, 9], 108, 4); % 108*4 double
    aList{i}=a;
end
save('aList.mat','aList');
```

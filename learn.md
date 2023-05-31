# 编程

## python

### 0.输入

```python
import sys
for line in sys.stdin:
    a = line.split()
    
a = input()
```



### 1.eval() 函数

> eval() 函数用来执行一个字符串表达式，并返回表达式的值。

```python
>>>x = 7 
>>> eval( '3 * x' ) 
21 
>>> eval('pow(2,2)') 
4 
>>> eval('2 + 2') 
4 

a = eval(input())  # 将输入字符串转化为变量，如'[0,1,2]'

```

### 2.split()方法

> 通过指定分隔符对字符串进行切片
>
> ```Python
> str.split(str="", num=string.count(str))
> ```

```python
str.split(' ', 1 ) # 以空格为分隔符，分隔成两个

year, month = map(int,input().split())  # 将输入的字符已默认的空格分隔符分割,通过map函数，转为两个整型变量
```

### 3.strip()方法

> 用于移除字符串头尾指定的字符（默认为空格或换行符）或字符序列。不能删除中间部分的字符。
>
> ```python
> str.strip([chars]);
> ```

```python
str = "00000003210Runoob01230000000"; 
print str.strip( '0' );  # 去除首尾字符 0
# 3210Runoob0123
```

### 4.filter()函数

> 去除list中的空字符

```Python
list1 = ['122', '2333', '3444', '', '', None]
a = list(filter(None, list1))  # 只能过滤空字符和None
print(a)  # ['122', '2333', '3444']
```

### 5.set()函数

> 对list去重

```Python
list1 = list(set(list1))
```

### 6.floor函数、ceil函数、round函数

```Python
import math
# floor() 返回数字的下舍整数。
math.floor(100.12) :  100.0
# ceil() 函数返回一个大于或等于 x 的的最小整数。    
math.ceil(100.72) :  101
# round()返回浮点数x的四舍五入值。
round(80.23456, 2) :  80.23
```

### 7.list列表的增删改减

```Python
# 增
# append() 追加单个元素到List的尾部，参数可以是任何数据类型；
list1.append('c')
# extend() 将一个列表中每个元素分别添加到另一个列表中，只接受一个参数；
list2.extend(list1)
# insert() 将一个元素插入到列表中，参数有两个（如insert(1,”g”)），第一个参数是索引点，即插入的位置，第二个参数是插入的元素。
list1.insert(1,'x')

# 删
# 使用del删除对应下标的元素
del list1[2]
# 使用pop()删除最后一个元素
list1.pop()
# .删除指定值的元素
li.remove(4)
# 使用切片来删除
li = li[::-1]


```

### 8.字符替换

```python
str_ = '123\n'
str_.replace('\n','') # '123'
```

### 9.字符串拆解成列表

```python
srt_ = 'abc'
list(str_)  # ['a','b','c']
```

### 10.拼接列表成字符串

```python
list_ = ['a','b','c']
print("-".join(list_)) # 'a-b-c'
print("".join(list_)) # 'abc'
```

### 11.列表排序

```python
sorted(list_,key=None,reverse=False) # 默认False升序
sorted([3,2,1]) # [1,2,3]
sorted(['c','b','a']) # ['a','b','c']

# 倒序
a = ['c','a','r']
a[::-1] # ['r','a','c']
```

### 12.大小写转换

```python
str_ = 'A'
str_.lower() # a
str_.upper() # A
```

### 13.字典

```python
dict_ = {'1':'a','2':'b','3':'c'}

dict_.items() 	#[('1', 'a'), ('2', 'b'), (3, 'c')]
dict_.keys() 	#['1', '2', '3']
dict_.values()	#['a', 'b', 'c']
```

### 14.字符判定

```python
str.isupper() #判断s是否都是大写字母
str.islower() #判断s是否都是小写字母
str.istitle() #判断s中的每个单词首字母是否都是大写字母且其他位置无大写字母,要求每个单词必须用标点符号或空格分隔开来；
str.isspace(); #判断s是否都是空格
str.isdigit(); #判断s是否都是数字
str.isidentifier() #判断s是否一个合法的Python标识符
str.isprintable() #判断s是否都是可打印字符
```

### 15.进制转换

```python
# 2进制
bin(int(input()，8))		# 8->2
bin(int(input()，10))	# 10->2
bin(int(input()，16))	# 16->2
# 8进制	
oct(int(input()， 2))	# 2->8
oct(int(input()，10))	# 10->8
oct(int(input()，16))	# 16->8
# 10进制	
int(input()，2)			# 2->10
int(input()，8)			# 8->10
int(input()，16)			# 16->10
# 16进制	
hex(int(input()， 2))	# 2->16
hex(int(input()，8))		# 8->16
hex(int(input()，10))	# 10->16
```



## C++

### 1.输入输出

```c++
#include <iostream>
cin >> a;  //输入
cout<< b;  //输出

#include<stdio.h>
scanf("%d",&num);  //通过scanf("%s",str)==1判断是否读取结束，0表示结束
printf("%d",num); //%d、%f、%s、%c 是最常用的，它们分别是输出整数、实数、字符串和字符的控制符

```



### 2.STL容器

#### 2.1 vector

**vector**是种容器，类似数组一样，但它的size可以动态改变。

```c++
#include<vector>
vector<int> v[100];

v.push_back(x) // 就是在vector容器v后面添加一个元素x
v.pop_back()   // 可以删除vector的尾元素
v.size()       // 用来获得vector中元素的个数
v.clear()      // 用来清空vector中的所有元素
v.insert(it, x)//用来向vector的任意迭代器it处插入一个元素x，
    		   // v.insert(v.begin() + 2, -1);	//将-1插入v[2]的位置：
v.insert(pos,first,last) //在 pos 位置之前，插入其他容器中位于 [first,last) 区域的所有元素(容器拼接)。
    					 //v.insert(v.end(), v1.begin(), v1.end());  // 将v和v1拼接在一起
    
v.erase(it)          // 即删除迭代器为it处的元素：v.erase(v.begin() + 2);	//删除元素v[3]
v.erase(first, last) // 即删除[first, last）内的所有元素：v.erase(v.begin(), v.end())即清空所有元素

//输出
set<int>::iterator it; //遍历器
for(it=v.begin();it!=v.end();it++){
    cout<<*it<<" ";
}
v[1];  // 下标

//倒序
reverse(v.begin(). v.end())
```

#### 2.2 set

Set关联式容器，也叫集合，集合里是不能有重复的元素，以默认升序的排列方式排好的。

```c++
#include<set>
set<int> s;  // 创建set
s.insert(1); // 插入元素

*s.begin()	//返回set容器的第一个元素，set_.begin()是第一个指向该元素的迭代器，可以理解为指针，通过*访问元素
*s.end() 　　　//返回set容器的最后一个元素
s.empty() 　　//判断set容器是否为空
s.size() 　　 //返回当前set容器中的元素个数
s.count(x)   // x的个数（1或者0）
    
s.clear()    //删除set容器中的所有的元素
s.erase(x)   //删除元素x
//输出
set<int>::iterator it;
for(it=s.begin();it!=s.end();it++){
    cout<<*it<<" ";
}
```

#### 2.3 map

map为映射,也是常用的STL容器，map可以将任何基本类型（包括STL容器）映射到任何基本类型（包括STL容器）**map**会以***\*键\*******\*从小到大的顺序自动排序\****

```c++
#include<map>
map<char, int> m; 
m['c'] = 20;

map<char, int>::iterator it=m.begin();  // map会以键从小到大的顺序自动排序
	cout << it->first;	      //it->first来访问键
	cout << it->second; 	  //it->second来访问值

m.size()  // 用来获得map中映射的对数
m.clear() // 用来清空map中的所有元素
    
m.erase(key) // key为要删除的映射的键
m.erase(first, last) // first，last为迭代器的地址

map<char , int>::iterator it;
it = m.find("z"); // 查看key是否存在
if(it!=m.end())   // 如果查找失败，则返回end()函数所在的迭代器
    it->second;
```

#### 2.4 queue

```c++
#include<queue>
queue<int> q;

q.push()   // 在队尾插入一个元素
q.pop()    // 删除队列第一个元素
q.size()   // 返回队列中元素个数
q.empty()  // 如果队列空则返回true
q.front()  // 返回队列中的第一个元素
q.back()   // 返回队列中最后一个元素
```



#### 2.x

```c++
#include<algorithm>
//1.排序
sort(a.begin(),a.end()); //对a中的从a.begin()（包括它）到a.end()（不包括它）的元素进行从小到大排列
//2.倒置
reverse(a.begin(),a.end()); //对a中的从a.begin()（包括它）到a.end()（不包括它）的元素倒置，但不排列
//3.复制
copy(a.begin(),a.end(),b.begin()+1); //把a中的从a.begin()（包括它）到a.end()（不包括它）的元素复制到b中，从b.begin()+1的位置（包括它）开始复制，覆盖掉原有元素
//4.查找
find(a.begin(),a.end(),10); //在a中的从a.begin()（包括它）到a.end()（不包括它）的元素中查找10，若存在返回其在向量中的位置
```







### 3.排序

```c++
//sort

//数组
int a[10];
sort(a, a +10);  //10最后一位不取
sort(a, a +10, greater<int>) //默认升序，greater<int>表示降序
//vector、set
vector<string> v;
sort(v.begin(), v.end());  //10最后一位不取


//自定义
bool cmp(int num1, int num2) {
    return num1 > num2;     // 可以简单理解为 > 降序排列;  <  升序排列
}
sort(a, a + 10, cmp);  // 使用自定义排序函数

//自定义结构体
struct Student {    // 学生结构体
    string name;    // 学生姓名
    int grade;      // 学生分数
};
bool cmp(Student s1, Student s2) {  // 自定义排序
    if (s1.grade != s2.grade) {     // 如果学生成绩不同
        return s1.grade > s2.grade; // 则按照成绩降序排列
    }
    return s1.name < s2.name;   // 否则按照姓名升序排列
}

```

### 4.string

```c++
//1.拼接
string s="a";
s +="bc"; // 直接相加

string s2="123";
str3.append(str4,2,3); //从第二个开始到结束的3个字符

//2.替换
string s2=s.replace(0,1,"A"); // 0到1位替换 a->A
#include<algorithm>
replace(s2.begin(), s2.end(), 'a', 'A'); // 替换指定单字符

//3.查找
int pos1=s.find("a",0); // 从0开始左向右寻找字符第一个次出现的位置
int pos2=s.rfind("v",s.size()); // 从s.size开始右向左，查不到返回-1

//4.插入，删除
string s="234"；
s.insert(0,"01"); //从0位置插入
s.append(5, '.'); //从最后的位置插入 5 个 '.'，可以是char类型
s.append('.');    //从最后的位置插入char类型
s.erase(0,2);     //删除[0,2)
#include<algorithm>
s.erase(remove(s.begin(),s.end(),'0'),s.end());  // 删除指定字符

//5.截取
string s2=s.substr(0,2); //截取 从0开始，长度为2的字符串

//6.string转int
string s="123"
const char* c = s.c_str();
int a = atoi(c);  //atoi函数跳过前面的空白字符，直到遇上数字或正负符号才开始做转换，而再遇到非数字才结束转换，无法转返回0

//7.切割
stringstream ss(str);
string item;
vector<string> elems;
while (getline(ss, item, '')) {
	elems.push_back(item);
}
```



### 5.移位

```c++
// 10.0.3.193 -> 167969729
unsigned int output_10 = 0;  // 占4个字节，可以移位
output_10 += 10 << 24;
output_10 += 0 << 16;
output_10 += 3 << 8;
output_10 += 193 << 0;

// 167773121 -> 10.3.3.193
int a = 0;
unsign int = 167773121;
a = ip_10 >> 24;
cout << a << '.';
a = (ip_10 >> 16) & 255;  // &位运算 167773121 与 0x00 00 00 ff相乘
cout << a << '.';
a = (ip_10 >> 8) & 255;
cout << a << '.';
a = (ip_10 >> 0) & 255;
cout << a;
```

### 6.参数

```c++
//形参: 在函数定义中出现的参数可以看做是一个占位符，它没有数据，只能等到函数被调用时接收传递进来的数据。
int add(int m,int n){...};
//实参: 函数被调用时给出的参数包含了实实在在的数据，会被函数内部的代码使用，所以称为实际参数，简称实参。
add(6,9);
//形参和实参的功能是传递数据，发生函数调用时，实参的值会传递给形参。



//值传参: 形参改变，实参是没有变化的。
void swap(int p1, int p2)
//指针传参: 指针传递的本质还是值传递，只是传递的值是地址。
void swap(int *p1, int *p2)
//引用传参: 引用传递，传递的是变量本身能保证参数传递中不产生副本，提高传递的效率，且通过const的使用，保证了引用传递的安全性。
void swap(int &p1, int &p2)
```

### 7.二叉树

```c++
// 自定义结构体 二叉树
struct TreeNode {
    int val;  // 当前节点的值
    TreeNode *left;  // 左子树节点指针
    TreeNode *right;  // 右子树节点指针
    TreeNode(int x) : val(x), left(NULL), right(NULL) {}  //创建节点TreeNode* T1 = new TreeNode(8);
};

//dfs深度优先搜索
void Traversal(TreeNode* root) {
    if(!root)
        return;
    // cout<<root->val<<" "; 先序遍历（根，左，右）
    preorderTraversal(root->left);
    // cout<<root->val<<" "; 中序遍历（左，根，右） 
    preorderTraversal(root->right);
    // cout<<root->val<<" "; 后序遍历（左，右，根） 
}

//bfs广度优先搜索
void levelOrder(TreeNode *root){
    queue<TreeNode*> q;
    q.push(root);
    while(!q.empty()){
    	int n=q.size();
        for(int i=0;i<n;++i){
            TreeNode *temp=q.front();
            if(temp){
                q.push(temp->left);
                q.push(temp->right);
                cout<<temp->val<<" ";
            }
            q.pop();
         }
    }
}

```







## 笔经

2.  数组和列表的区别

   > 概述：
   >
   > python本身并没有数组类型，但是他的Numpy库中有数组类型。python中的list是python的内置数据类型，list中的数据类不必相同的，而array的中的类型必须全部相同。
   >
   > 区别：
   >
   > 1. 二者都可以用于处理多维数组。
   >
   > Numpy中的ndarray对象用于处理多维数组，它作为一个快速而灵活的大数据容器。Python列表可以存储一维数组，通过列表的嵌套可以实现多维数组。
   >
   > 2. 存储效率和输入输出性能不同。
   >
   > Numpy专门针对数组的操作和运算进行了设计，存储效率和输入输出性能远优于Python中的嵌套列表，数组越大，Numpy的优势就越明显。
   >
   > 3. 元素数据类型。
   >
   > 通常，Numpy数组中的所有元素的类型都必须相同的，而Python列表中的元素类型是任意的。
   >
   > 

2. C++进程与线程的区别

   > 进程是操作系统分配资源的基本单位，而线程是 CPU 调度和分派的基本单位。
   > 进程有自己独立的地址空间，而线程共享进程的地址空间。
   > 一个进程可以包含多个线程，每个线程并行执行不同的任务。

3.  重载

   > 函数名称必须相同。
   > 参数列表必须不同（个数不同、类型不同、参数排列顺序不同等）。
   > 函数的返回类型可以相同也可以不相同。
   > 仅仅返回类型不同不足以成为函数的重载。
   >
   > *为什么C不支持函数重载，C++确能支持函数重载？*
   >
   > ​	因为C语言的函数名修饰规则与函数参数无关，或者说没有修饰规则。
   >
   > ​	而C++在编译期间，会将函数名修饰一下，即将函数名与参数联系在一起。如：function(float a, char b) : function_float_char

4. TensorRT加速原理

   > TensorRT，是nvidia发布的dnn推理引擎，是针对nvidia系列硬件进行优化加速，实现最大程度的利用GPU资源，提升推理性能，提高在激活函数的推理速度

5. **Lambda** 

   > Lambda函数也被称为匿名(没有名称)函数，它直接接受参数的数量以及使用该参数执行的条件或操作，该参数以冒号分隔，并返回最终结果。
   >
   > ```python
   > g = lambda x : x**2  # 输入x，返回x**2
   > g(4) # 16
   > 
   > 
   > f = lambda x: 'even' if x%2==0 else 'odd'  # 输入x，返回奇偶数
   > f(4) # odd
   > 
   > lst = [1,2,3,4,5]
   > res = list(map(lambda x:x*x, lst)) # 1,4,9,16,25 以函数作为map的第一个参数
   > ```

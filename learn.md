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



## C++上机

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
vector<int> v(26, 0);
vector<int> v1 = v;
vector<int> v2(v);

v.push_back(x) // 就是在vector容器v后面添加一个元素x
v.pop_back()   // 可以删除vector的尾元素
v.size()       // 用来获得vector中元素的个数
v.clear()      // 用来清空vector中的所有元素
v.insert(it, x)//用来向vector的任意迭代器it处插入一个元素x，
    		   // v.insert(v.begin() + 2, -1);	//将-1插入v[2]的位置：
v.insert(pos,first,last) //在 pos 位置之前，插入其他容器中位于 [first,last) 区域的所有元素(容器拼接)。
    					 //v.insert(v.end(), v1.begin(), v1.end());  // 将v和v1拼接在一起
    
v.erase(it)          // 即删除迭代器为it处的元素：v. erase(v.begin() + 2);	//删除元素v[3]
v.erase(first, last) // 即删除[first, last）内的所有元素：v.erase(v.begin(), v.end())即清空所有元素

//输出
set<int>::iterator it; //遍历器
for(it=v.begin();it!=v.end();it++){
    cout<<*it<<" ";
}
v[1];  // 下标

//倒序
reverse(v.begin(). v.end())
    
// 查找
if (std::find(v.begin(), v.end(), key) != v.end())
```

#### 2.2 set

Set关联式容器，也叫集合，集合里是不能有重复的元素，以默认升序的排列方式排好的。

```c++
#include<set>
set<int> s;  // 创建set
s.insert(1); // 插入元素

*s.begin()	 //返回set容器的第一个元素，set_.begin()是第一个指向该元素的迭代器，可以理解为指针，通过*访问元素
*s.end() 　　 //返回set容器的最后一个元素
*s.rbegin()  //返回指向集合中最后一个元素的反向迭代器
*s.rend()    //返回指向集合中第一个元素的反向迭代器
s.empty() 　　//判断set容器是否为空
s.size() 　　 //返回当前set容器中的元素个数

// 查找
s.count(x)   // x的个数（1或者0）
s.find(x) != s.end();

// 删除
s.clear()    //删除set容器中的所有的元素
s.erase(x)   //删除元素x
//输出
set<int>::iterator it;
for(it=s.begin();it!=s.end();it++){
    cout<<*it<<" ";
}


# multiset
//能时刻保证序列中的数是有序的，而且序列中可以存在重复的数
multiset<int> s; // 存有序可重复：1 1 2 3 4 5 5
s.erase(x)   // 删除所有元素x
auto it = s.find(x);
s.erase(it) // 这里是删除其中的一个x; 删除的是一个位置
```

#### 2.3 map

map为映射,也是常用的STL容器，map可以将任何基本类型（包括STL容器）映射到任何基本类型（包括STL容器）**map**会以***\*键\*******\*从小到大的顺序自动排序\****

```c++
#include<map>
map<char, int> m; 
m['c'] = 20;
m.emplace('c', 20);

map<char, int>::iterator it=m.begin();  // map会以键从小到大的顺序自动排序
	cout << it->first;	      //it->first来访问键
	cout << it->second; 	  //it->second来访问值

m.size()  // 用来获得map中映射的对数
m.clear() // 用来清空map中的所有元素
    
m.erase(key) // key为要删除的映射的键
m.erase(first, last) // first，last为迭代器的地址

// 查看key是否存在
m.count(key) == 1;
map<char , int>::iterator it;
it = m.find(key); 
if(it!=m.end())   // 如果查找失败，则返回end()函数所在的迭代器
    it->second;

// unorder_map 无序的map
unorder_map<char, int> u_m; 
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
    

// 遍历
int size = q.size();
for(int i = 0; i < size; i++) { // 无法用迭代器变量，只能在原本size下，先push，再pop
    cout << q.front() << endl;
    q.push(q.front());
    q.pop();
}    
    
    
//优先队列 priority_queue
//priority_queue<Type, Container, Functional>
priority_queue<int> q;  // 默认vector，队首q.top()最大
priority_queue<int,vector<int>,less<int>> q;	// 队首q.top()最大
priority_queue<int,vector<int>,greater<int>>q;  // 队首q.top()最小
priority_queue<int, vector<int>, decltype<&cmp>> q(cmp); // cmp为比较函数
// pair
priority_queue<pair<int, int>>q;  // pair 先比较第一个int，再比较第二int
// struct
struct fruit {
    string name;
    int price;
};
struct cmp {
    bool operator ()(fruit fl,fruit f2)
    {
        return f1.price > f2.price; // true表示 优先级 f1 < f2, f2放前面 （容易混淆）
    }
};
priority_queue<fruit,vector<fruit>,cmp> q; // 队首q.top().price最小
```



#### 2.5 stack 

栈是基本的数据结构之一,特点是 **先进后出**

```c++
stack<int> st; 
st.push(x);     // 将x压入栈顶
st.top();       // 返回栈顶元素
st.pop();       // 删除栈顶元素
st.size();      // 返回栈中元素的个数
st.empyt();     // 检查栈是否为空
```



#### 2.x

```c++
// pair<type1, type2> p;
pair<type1, type2> p;
pair<int, std::string> p1 = { 1, "kenny" };
pair<int, char> p2 = std::make_pair(1, 'a');

p.first  // 访问第一个元素
p.second // 访问第二个元素


// tuple
tuple<type1, type2, type3, ...> t;   
tuple<int, double, string> t1(1, 15.4, "James");
tuple<int, double, string> t2 = make_tuple(1, 15.4, "James");
get<0>(t1) // 访问第一个元素
get<1>(t1) // 访问第二个元素
get<2>(t1) // 访问第三个元素
    

// emplace 对比push，支持隐式构造
vector<vector<int>> v;
v.emplace_back(vector<int>{1,2,3});
vector<pair<int, int>> v;
v.emplace_back(1,2);
```

#### 2.0 

```c++
#include<algorithm>
// 1.排序 //

//数组
int a[10];
sort(a, a +10);  //10最后一位不取
sort(a, a +10, greater<int>) //默认升序，greater<int>表示降序
    
//vector、set
vector<string> v;
sort(v.begin(), v.end());    //正向排序 小 -> 大
sort(v.rbegin(), v.rend());  //逆向排序 大 -> 小


//自定义
bool cmp(int num1, int num2) { // 基础类型
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
sort(v.begin(), v.end(), cmp);  // 使用自定义排序函数


// 自定义STL
// 自定义函数cmp需要放在类之外，如果放类里面需要加static，因为隐藏带有this，sort函数无法匹配。
// 如果需要成员变量，考虑lambda捕获 auto cmp = [a_, b_]();
bool cmp(tuple<int, string ,int> t1, tuple<int, string ,int> t2) {  // 自定义排序
    if (get<2>(t1) != get<2>(t2)) {     // 如果价格不同
        return get<2>(t1) > get<2>(t2); // 则按照价格降序排列
    }
    return get<1>(t1) < get<1>(t2);   // 否则按照名字升序排列
}
vector<tuple<int, string ,int>> v{{1, "c", 1} {2, "b", 1} {3, "a", 3} // 编号，名字，价格
sort(v.begin(), v.end(), cmp);  // 使用自定义排序函数


// 2.倒置 //                                  
reverse(a.begin(),a.end()); //对a中的从a.begin()（包括它）到a.end()（不包括它）的元素倒置，但不排列
                                  
// 3.复制 //
copy(a.begin(),a.end(),b.begin()+1); //把a中的从a.begin()（包括它）到a.end()（不包括它）的元素复制到b中，从b.begin()+1的位置（包括它）开始复制，覆盖掉原有元素
                                  
// 4.查找 //
find(a.begin(),a.end(),10); //在a中的从a.begin()（包括它）到a.end()（不包括它）的元素中查找10，若存在返回其在向量中的位置                                  
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

### 8.数字与字符

```c++
string s;
char c;
int i;
double d;

// string -> int、double
i = atoi(s), i = atof(s) 

// int、double -> string
s = to_string(i)

// char[] -> int、double
i = (int)c
    
// int -> char
c = i + '0'; //ascii码

// char -> int
i = c - '0'
    
    
// atoi(), atol()
int i = atoi("123", nullptr, 10); // 将10进制的srting转为10进制int
int i = atoi("FF", nullptr, 16); // 将16进制的srting转为10进制int
int i = atoi("10101010", nullptr, 2); // 将2进制的srting转为10进制int
long int l = atoi("12345678", nullptr, 10); // 将10进制的srting转为10进制long


// bitset
#include <bitset>
bitset<N> bitset1; // 创建一个长度为 N 的 bitset，所有位都被初始化为 0
bitset<N> bitset2(value); // 使用二进制整数 value 初始化一个长度为 N 的 bitset
bitset<N> bitset3(string); // 使用二进制字符串 string 初始化一个长度为 N 的 bitset
bitset<N> bitset4(bitset); // 使用另一个 bitset 初始化一个长度为 N 的 bitset

bitset<8> bs(10);          // 00001010
bitset<8> bs (0x0A);       // 00001010
bitset<8> bs ("00001010"); // 00001010

string str = bs.to_string();
int i = bs.to_ulong();
long int l = bs.to_ullong();
```

















## C++基础知识

### 基础语法

```c++
//1. ++
int i = 0, j = 0;
j = i++; //右++返回的是++之前的值 j=0,i=1
j = ++i  //左++返回的是++之后的值 j=2,i=2



//2. 函数局部变量
char * G()
{
	char g[20] = "Beijing";
	return g;
}// error：函数中的局部变量存放在stack中，函数执行完成之后会自动释放，因此不应将局部变量的指针作为返回值。



//3. 正码, 反码, 补码
char i = 10;
//0 0001010 10原码
//1 0001010 -10原码

//00001010 正数的反码和原码一样
//11110101 负数的反码就是在其原码的基础上 符号位不变 其他位取反。

//00001010 正数的补码就是其原码
//11110110 负数的补码就是在其反码的基础上+1
//计算机系统中，数值一律用补码来表示：因为补码可以使符号位和数值位统一处理，同时可以使减法按照加法来处理。



//4. 指针调用函数
max(int a, int b);
int (*pf)(int,int);  
pf = max;
(*pf)(100,100);// 括号不能少



//5. 数组定义
char a[]="abcde"; 					//字符串：  a的内存占用为5个字符 + /0字符串结束字符，长度为6
char b[]={'a', 'b', 'c', 'd', 'e'};	//字符数组：b的内存占用为5个字符，长度为5



//6. sizeof
sizeof(object)  //其作用是返回一个对象或类型所占的内存字节数。
	// 结构体
    struct S1  
    {  
        char a;  
        int b;  
    };  
	sizeof(S1); //值为8，字节对齐，在char之后会填充3个字节。b的offset = 4;
				//结构体每个成员相对于结构体首地址的偏移量（offset）都是（这个）成员大小的整数倍，如有需要编译器会在成员之间						加上填充字节。
    // 数组
    	char a[]="abcde"; //当字符数组表示字符串时，其sizeof值将’/0’计算进去。sizeof(a) = 6 
		void f(char a[])  //当数组为形参时，其sizeof值相当于指针的sizeof值。 sizeof(a) = 4
    // 类
    	类内部的成员变量：
			普通的变量：是要占用内存的，但是要注意对齐原则（这点和struct类型很相似）。
			static修饰的静态变量：不占用内容，原因是编译器将其放在全局变量区。
		类内部的成员函数：
			普通函数：不占用内存。
			虚函数：要占用4个字节，用来指定虚函数的虚拟函数表的入口地址。和虚函数的个数是没有关系的
    

//7. C++内置类型所占字节数
bool			1
char			1
short			2
int				4
unsigned int	4
long			4
unsigned long	4
long long		8
float			4
double			8
long double		8
char * (指针)	   4
    
            
//8. 重载
    // 重载需要在同一作用域     
    int func(int a, double b);
    int func(double b, int a);//构成重载：无论返回值，只看返回类型
	void func(char); 
    void func(int)//short -> int: 调用时，类型匹配向精度高的匹配
      
        
//9. include
#include ".h"	// 从当前项目目录下搜寻
#include <.h>	// 从系统include目录下，可以在环境变量下指定 
  
        
//10. 指针
int  var = 20;     
int * ptr = &var;   
int ** pptr = &ptr; 

Value of var: 20
Value of &var: 0x7ffce63490bc    (var的地址)

Value of ptr: 0x7ffce63490bc    (等于&var)
Value of *ptr: 20        (等于var)
Value of &ptr: 0x7ffce63490b0    (ptr的地址)

Value of pptr: 0x7ffce63490b0    (等于&ptr)
Value of *pptr: 0x7ffce63490bc    (等于ptr, 等于&var)
Value of **pptr: 20        (等于*ptr, 等于var)
Value of &pptr: 0x7ffce63490a8    (pptr的地址)
```

### 内存

```c++
//1. 申请与释放内存
char *buf = new char[20];
delete[] buf;  	// new/delete要匹配
char *buf_ = (char *)mallor(20);  // 显式指定字节数
free(buf_);		// mallor/free


//2. 内存管理
bss段
	通常是指用来存放程序中未初始化的全局变量的一块内存区域。初始化为0的全局变量会先放在bss
data段
	数据段通常是指用来存放程序中已初始化的全局变量的一块内存区域。有初值的全局变量和static变量在data区
text段
	代码段通常是指用来存放程序执行代码的一块内存区域。
heap
	堆是用于存放进程运行中被/*动态*/分配的内存段，它的大小并不固定，可动态扩张或缩减。
	当进程调用malloc等函数分配内存时，新分配的内存就被动态添加到堆上（堆被扩张），
    当利用free等函数释放内存时，被释放的内存从堆中被剔除（堆被缩减）。
stack
	栈又称堆栈，是用户存放程序临时创建的局部变量，
	在函数被调用时，其参数（函数形参）也会被压入发起调用的进程栈中，并且待到调用结束后，函数的返回值也会被存放回栈中。

```



### 关键字

```c++
//1. static
1. 全局静态变量：	在全局变量前加上关键字static
				作用域：全局静态变量在声明他的文件之外是不可见的，准确地说是从定义之处开始，到文件结尾。

2. 局部静态变量：	在局部变量之前加上关键字static
				作用域：作用域仍为局部作用域，当定义它的函数或者语句块结束的时候，作用域结束。但是当局部静态变量离开作用域后，						并没有销毁，而是仍然驻留在内存当中，只不过我们不能再对它进行访问，直到该函数再次被调用，并且值不变；

3. 静态函数：	 在函数返回类型前加static
    			函数的定义和声明在默认情况下都是extern的，但静态函数只是在声明他的文件当中可见，不能被其他文件所用。

4. 类的静态成员：	在类的成员变量前加static
				在类中，静态成员是类的所有对象中共享的成员，而不是某个对象的成员。静态数据成员只存储一处，供所有对象共用

5. 类的静态函数：	在类的成员函数前加static
				静态成员函数和静态数据成员一样，它们都属于类的静态成员，它们都不是对象成员。在静态成员函数的实现中可以引用类中					说明的静态成员。而如果静态成员函数中要引用非静态成员时，可通过对象来引用。
    			调用静态成员函数使用如下格式：<类名>::<静态成员函数名>(<参数表>);

    
//2. inline
普通函数频繁调用的过程消耗栈空间，每次调用函数都需要压栈，然后出栈。
为了消除函数调用的时空开销，在编译时将函数调用处用函数体替换，类似于C语言中的宏展开。在函数调用处直接嵌入函数体。
可以理解为内联函数的关键词是：替换
    
    
//3. extern
    //声明外部变量，供其它文件使用
	//a.h
        extern int a; // 声明，在外部文件定义
		extern int func();
	//b.cpp
		int a = 1;  // 定义（只能在一个文件下定义）
		int func(){...}
	//c.cpp
		printf(a);  // 调用
		func(a);

	 //extern "C"
		{ 
			#include "b.h"  //在CPP文件中include C头文件时，需要使用extern "C",
		} //C语言没有函数重载这一特性，C和C++编译这个函数的符号名可能类不一样。


//4. const
	1.const修饰普通类型的变量
        const int a = 1; // a的值不能被改变
    2.const 修饰指针变量
        const int *p = 8; //指针指向的内容 8 不可改变。简称左定值，因为 const 位于 * 号的左边。
        int a = 8;
        int* const p = &a;
		*p = 9; // const 指针 p 其指向的内存地址不能够被改变，但其内容可以改变。简称，右定向。因为 const 位于 * 号的右边。
    3.const参数传递和函数返回值
        const char* func(const char* c)//保护参数和返回值
    4.const修饰类成员函数
        class{
            int func() const {}; // 不能改变成员变量
        }

	5. 
        typedef int d;
		typedef d* D;
		const D did; // 相当于int* const did 容易混淆
```

### 构造析构

```c++
//1. 析构函数
父类的析构函数一般需要设置为虚函数
当我们使用基类的指针管理派生类，使用delete释放该指针时，会调用基类的析构函数~Base
如果基类的析构函数是虚函数，那么就会调用派生类的析构函数~Derived，再调用基类的析构函数~Base；（派生类的指针指向派生类也如此）
    
析构函数只能有一个，不能重载

//2. 构造函数
派生类对象初始化先调用基类构造函数，完成派生类中继承到的基类成员的初始化，再调用派生类的构造函数，完成派生类独自成员的初始化。
构造函数可以重载，但不能为虚函数
    
使用初始化列表对成员变量进行初始化时，初始化顺序与列表顺序无关，只与类内定义的顺序有关；
    
在构造函数里调用虚函数会报错，因为构造函数执行前，虚函数的映射还没建立
    
不能在构造函数使用可能会失败的语句，如：
    pthread_create() 
    socket()
    open()
    
//3. 拷贝构造函数
    class Class_{
    public:
        int a;
        Class_(const Class_ & c){a = c.a};  //拷贝构造函数的参数一定要是对象引用，否则会形参一直拷贝
    };

	1. 当用一个对象去初始化同类的另一个对象时，会引发复制构造函数被调用。
    Class_ c2(c1);
    Class_ c2 = c1;
	
	2. 函数 F 的参数是类 A 的对象，那么当 F 被调用时，类 A 的复制构造函数将被调用。
    void Func(Class_ c){}; // 调用拷贝构造函数
	void Function(const Class_ & c){}; // 引用则不会调用拷贝构造函数，减少开销

	3.函数的返冋值是类 A 的对象，则函数返冋时，类 A 的复制构造函数被调用。
    Class_ Func() {
    	Class_ c(4);
    	return c;}
	Func();

	4. 对于拥有其他资源的对象，复制操作需要深拷贝
    class Class_ {
    public:
        int* m_pArr;
        Class_() {m_pArr = new int[m_iCount];}
        Class_(const Class_& rhs) {
            m_pArr = new int[m_iCount];  // 不能让两个对象指向同一内存，需要重新new
            for (int i = 0; i < m_iCount; i++)
                m_pArr[i] = rhs.m_pArr[i];
        }
    };

	5. 派生类的拷贝构造函数
    C::C(const C &c1): B(c1) {…}


//4. 移动构造函数
复制构造：在对象被复制后临时对象和复制构造的对象各自占有不同的同样大小的堆内存，就是一个副本。
移动构造：就是让这个临时对象它原本控制的内存的空间转移给构造出来的对象，这样就相当于把它移动过去了。
class_name(class_name && ) // 右值  std::move(c)可以强制转成右值
    Class_(Class_&& c){
        a = c.a;
	    c.a= null;
	}
```

### 继承

| **类成员/继承方式**     | **public继承**        | **protected继承**     | **private继承**     |
| ----------------------- | --------------------- | --------------------- | ------------------- |
| **基类的public成员**    | 派生类的public成员    | 派生类的protected成员 | 派生类的private成员 |
| **基类的protected成员** | 派生类的protected成员 | 派生类的protected成员 | 派生类的private成员 |
| **基类的private成员**   | 在派生类中不可见      | 在派生类中不可见      | 在派生类中不可见    |

```c++
//1. 访问限定符
    1. public修饰的成员在类外可以直接被访问。
    2. protected在类外不能直接被访问，派生类中能访问。
    3. 基类private成员在派生类中无论以什么方式继承都是不可见的。
    4. class的默认访问权限为private，struct为public
    
//2. 同名成员变量和成员函数
    1. 同名的成员变量：访问同名成员变量，编译器是以子类为优先；想要访问父类的该成员变量，就需要加上修饰base::name
    2. 同名的成员函数：成员函数名字相同构成了隐藏。（函数重载是在同一个作用域，这里父类和子类是两个作用域）
		函数的隐藏，编译器会默认调用子类中匹配的函数（即使参数列表不一样），如果没有编译器就会报错

```

### 多态

```c++
//1. 虚函数
当我们使用基类的指针管理派生类，如果基类的函数virtual func()是虚函数，那么就会调用派生类的函数func(),实现多态
    
//2. 纯虚函数
	virtual void func() = 0;
	纯虚函数只做声明，不做定义。所以纯虚函数不能被执行，所在对象也不能被实例化。需要交给后续派生类实现。
```

### 异常

```c++
// 异常捕获
try{
    throw BarException();
}
catch(const Fooexception& e){ // 异常捕获选择const &
}
  
```



### 命名空间

```c++
using directive 	//指令: 把名字空间中的所有名字引入到当前作用域
    using namespace std;
    
using declaration	//声明: 是把名字空间的某个名字引入到当前作用域中
    using std::vector;

// 类的声明只能是using declaration
// 冲突：命名空间存在相同成员元素，存取时不会有冲突，使用时才会

int a = 1;
namespace Outer{
    int a = 2;
}
namespace Outer{
    namespace Inter{
    	int a = 3;
}
}

using namespace Outer;

int main(){
    int a = 4;
    cout << a; 				// 4临时变量
    cout << ::a;			// 1全局变量
    cout << Outer::a;		// 2
    cout << Outer::Inter::a;// 3
}
```

### 函数指针

```c++
//函数指针
函数的返回值类型（*指针名）（函数的参数列表类型）
    int Add(int x, int y){};
	int (*pf)(int, int) = &Add;
	int ret=(*pf)(3,5);

typedef int (*ADD)(int, int); //ADD为返回int类型的函数指针
//等同：int（*ADD)(int, int);
函数实现：
int *add(int, int){};			//add返回int类型的指针
ADD calc_func(int x, int y){	//ADD为返回int类型的函数指针
  return add(x + y);
}


//指针函数
_type_ *function(int, int) //返回的是指针地址
int function(int，int)     //返回的是int型数据。
    
int *fun(int x, int y)  //指针函数的定义
int* fun(int x, int y)   //指针函数的定义
```

### 智能指针

```c++
//1. unique_ptr
	# unique_ptr对象包装一个原始指针，并负责其生命周期。当该对象被销毁时，会在其析构函数中删除关联的原始指针。
	std::unique_ptr<Task> taskPtr(new Task(5));
	// make_unique
	# make_unique函数使用起来比直接用new操作符分配内存然后传递给unique_ptr更加安全，能够避免内存泄漏等问题。
	auto taskPtr = std::make_shared<Task>(5);

//2. shared_ptr
	# 不同的shared_ptr对象可以与相同的指针相关联，并在内部使用引用计数机制来实现这一点。
	std::shared_ptr<int> p1 = std::make_shared<int>();
	*p1 = 78; // p1.use_count() = 1
	std::shared_ptr<int> p2(p1); // p2.use_count() = p1.use_count() = 2

```



### 单例模式

```C++
单例模式:在整个系统生命周期内，保证一个类只能产生一个实例，确保该类的唯一性。

//1. 懒汉式：系统运行中，实例并不存在，只有当需要使用该实例时，才会去创建并使用实例。这种方式要考虑线程安全。
class CSingleton  
{  
public:  
    static CSingleton* GetInstance()  
    {  
         if ( m_pInstance == NULL )    
             m_pInstance = new CSingleton();  
         return m_pInstance;  
    }  
private:  
    CSingleton(){};  
    static CSingleton * m_pInstance;  
};  

//2. 饿汉式：系统一运行，就初始化创建实例，当需要时，直接调用即可。这种方式本身就线程安全，没有多线程的线程安全问题。
class CSingleton    
{    
public:    
    static CSingleton * GetInstance()    
    {    
        static CSingleton instance;     
        return &instance;    
    } 
private:    
    CSingleton(){}; 
};    
```

### 重载

```c++
C++规定重载运算符的操作对象至少有一个不是标准类型，而是用户自定义的类型， 比如不能重载 1+2
// 对象操作符重载
	//以全局函数的形式重载
    friend Complex operator+(const Complex &c1, const Complex &c2);
    //成员函数重载
    Complex & operator+=(const Complex &c);
```



### Gtest

```c++
// TODO
```

### 华为C++规范

```c++
// 

x = a + b & 5; // &优先级比+低


// 动态内存
auto ptr = std::make_unique() //使用make_unique 而不是new，delete
    
    
// 常量
constexpr int a = 0;
#define A 0 //避免使用宏来定义常量


// 枚举
enum class myenum{
} // 优先使用枚举类型而不是普通枚举 enum myenum


// 继承转换
Base* base_object;
Derived* derived = dynamic_cast<Derived*>(base_object); // dynamic_cast强制转换


// 模板
模板的所有部分和显示特殊化都必须放在该模板本身所在的文件中
比如在foo.h文件定义模板类Foo，template<>class FOO()显示特殊化也得在foo.h中
    

// vector
std::vector<int> v;
for(size_t i = 0; i < v.size(); ++i)
    
    
// static、namespace
针对cpp文件中不需要导出的变量、常量或函数，应该使用匿名namespace封装或者使用static修饰，更推荐namespace
    
    
// 安全的成员函数
void Print(const MyClass& obj); // 引用比指针更安全


// 断言
static_assert();


// sprintf_s
spritf_s(buf, sizeof(buf), 'input something %d', x);
spritf_s(buf, sizeof(buf), 'input something %d%d', x, y);


// 类型转换
char 不能转 int
int 可以转 char float
    

// 虚函数
C++中，虚函数是动态绑定的，但函数的缺省参数却是在编译时就静态绑定的。这意味着你最终执行的函数是一个定义在派生类，但使用了基类中的缺省参数值的虚函数。为了避免虚函数重载时，因参数声明不一致给使用者带来的困惑和由此导致的问题，
    规定所有虚函数均不允许声明缺省参数值！
```

### 测试

```c++
// 1.测试覆盖
	语句覆盖：选择足够多的测试用例，使得程序中的每个可执行语句至少执行一次。
	判定覆盖：通过执行足够的测试用例，使得程序中的每个判定至少都获得一次“真”值和“假”值，也就是使程序中的每个取“真”分支和取“假”分				支至少均经历一次，也称为“分支覆盖”。
	条件覆盖：设计足够多的测试用例，使得程序中每个判定包含的每个条件的可能取值（真/假）都至少满足一次。
	判定/条件覆盖：设计足够多的测试用例，使得程序中每个判定包含的每个条件的所有情况（真/假）至少出现一次，并且每个判定本身的判定				结果（真/假）也至少出现一次。
	组合覆盖：通过执行足够的测试用例，使得程序中每个判定的所有可能的条件取值组合都至少出现一次。
	路径覆盖：设计足够多的测试用例，要求覆盖程序中所有可能的路径。

路径覆盖 > 条件组合 > 判定条件 > 条件覆盖 > 判定覆盖 > 语句覆盖  
        
        
        
//2 使用数据组合覆盖技术识别测试条件
 	EC		单一选择组合			每一个测试输入的每一个取值在所有组合中至少出现一次
 	BC		基本选择组合			以基本组合为基础，通过更改一个输入的取值创建新的组合
 	AC		全组合			  	每个测试输入的每个取值的所有可能组合
 	OA		正交数组		 	基于正交数组的组合方式
 	N:Wise	覆盖任意N个输入
        	的全组合的组合方式	覆盖任意N个输入的全组合的组合方式
        
//3. TEST        
TEST()当您想要为静态或全局函数或简单类编写单元测试时
TEST_F()当您需要访问单元测试中的对象和子例程时
TEST_P()当您想要使用参数编写测试时
        
//4. 静态测试和动态测试      
    静态测试是指测试不运行的部分：只是检查和审阅,如规范测试、软件模型测试、文档测试等。
    动态测试是通常意义上的测试，也就是运行和使用软件。
```

### GDB

```c++
// 查看函数参数
	b func
    continue
    Info args
        
// 死锁信息
    info thread 
        // 当前进程中所有线程的信息，包括线程 ID、状态、调用栈等信息。通过查看线程的调用栈，可以得知当前线程正在等待哪个互斥锁。
        
// 设置断点
    # 普通断点
	linenum	linenum 	是一个整数，表示要打断点处代码的行号。
	filename:linenum	filename 表示源程序文件名；linenum 为整数，表示具体行数。
	+ offset			+offset 表示以当前程序暂停位置（例如第 4 行）为准，向后数 offset 行处（第 6 行）打断点
	- offset			-offset 表示以当前程序暂停位置为准，向前数 offset 行处（第 2 行）打断点。
	function			function 表示程序中包含的函数的函数名，即 break 命令会在该函数内部的开头位置打断点
	filename:function	filename 表示远程文件名；function 表示程序中函数的函数名。
    # 条件断点
    b src/main.cpp:127 if cnt==10	当满足一定条件时才会触发
    # 数据断点
    b *address  		当该地址上的内容发生改变时就会触发断点。
        
// 监视断点
    对于监控 C、C++ 程序中某变量或表达式的值是否发生改变，watch 命令的语法非常简单，如下所示：
		(gdb) watch cond
	rwatch 命令：只要程序中出现读取目标变量（表达式）的值的操作，程序就会停止运行；
	awatch 命令：只要程序中出现读取目标变量（表达式）的值或者改变值的操作，程序就会停止运行。
        
// 查看内容
	x/<n/f/u> <addr>
    	x：examine命令，查看内存地址中的值
        n、f、u是可选的参数。
        n 是一个正整数，表示显示内存的长度。
		f 表示显示的格式。x 按十六进制格式显示变量。d 按十进制格式显示变量。
		u 表示从当前地址往后请求的字节数。u参数可以用下面的字符来代替，b表示单字节，h表示双字节，w表示四字 节，g表示八字节。
```

### Cmake

```cmake
1. 添加头文件目录
include_directories([AFTER|BEFORE] [SYSTEM] dir1 [dir2 ...])
2. 添加需要链接的库文件目录
link_directories(directory1 directory2 ...)
3. 查找库所在目录
find_library (<VAR> name1 [path1 path2 ...])
4. 添加需要链接的库文件路径
link_libraries(library1 <debug | optimized> library2 ...)
5. 设置要链接的库文件的名称
target_link_libraries(<target> [item1 [item2 [...]]] [[debug|optimized|general] <item>] ...)
6. 为工程生成目标文件
add_executable(<name> [WIN32] [MACOSX_BUNDLE]
               [EXCLUDE_FROM_ALL]
               source1 [source2 ...])
               
               
7.添加编译选项 # 不一定生效
add_compile_options（-g -Werror）
```



### STL性能

| 容器名称 | 插入/删除                                | 查找   | 使用场景                          |
| -------- | ---------------------------------------- | ------ | --------------------------------- |
| vector   | 尾端：O（1）、非尾端P：O（N-P）          | O（1） | 需要快速查找，不需要频繁插入/删除 |
| list     | O（1）                                   | O（N） | 需要频繁插入/删除，不需要快速查找 |
| deque    | 首尾端：O（1）非首尾P：O（min（p， N-P） | O（1） | 较少使用，建议用list/vector       |
| queue    | 只能尾端入、首端删除：O（1）             | 不支持 | FIFO（先进先出）                  |

### 线程与锁

```c++
// 当多个线程同时对共享数据进行读或写操作时，会发生一些难以预料的事。

# 利用两个线程来对同一个变量count进行10000次++操作。
void mythread(int &num) {
	for (int i = 0; i < 100000; i++) {
		num++;
	}
}
int count = 0;
thread mythread1(mythread, ref(count));
thread mythread2(mythread, ref(count)); // 最终count会远小于20000


	//1. 互斥量
mutex mymutex;
void mythread(int &num) {
	for (int i = 0; i < 100000; i++) {
		lock_guard<mutex> my_lock(mymutex);
		num++;	// count = 20000
	}
}



	//2. 原子操作
void mythread(atomic<int> &num) {
	for (int i = 0; i < 100000; i++) {
		num++;  // count = 20000
	}
}
atomic<int> count = 0;



// 互斥量mutex
C++11提供如下4种语义的mutex：
    std::mutex，独占的互斥量。
    std::time_mutex，带超时的独占互斥量。
    std::recursive_mutex，递归互斥量。
    std::recursive_timed_mutex，带超时的递归互斥量。
常用成员函数：
    lock() 		——互斥量加锁。线程调用该函数后存在 3 种情况：1). 如果该互斥量当前没有被锁住，则调用线程将该互斥量锁住，直到调						用unlock之前，该线程一直拥有该锁；2). 如果当前互斥量被其他线程锁住，则当前线程会阻塞；3). 如果当前线程						重复加锁，则会产生死锁deadlock)。
    unlock() 	——互斥量解锁。
    try_lock() 	——尝试加锁，如果互斥量已被其他线程加锁则当前调用立即返回，不阻塞。

    
// 原子操作atomic
优点
    执行效率比互斥量更高
    std::atomic来代表原子操作，是个类模板。其实std::atomic是用来封装某个类型的值的。
局限性
    一般只能用于变量的一些简单操作，如++、–、+=、-=、&=、|=、^=，其他操作不一定可以执行。
    通常在一些计数场景用的多。
    互斥量的加锁一般是针对一个代码段，而原子操作针对的一般都是一个变量。
    
    
 
#当使用volatile 声明的变量的值的时候，系统总是重新从它所在的内存读取数据，即使它前面的指令刚刚从该处读取过数据。 
#volatile和多线程没有关系！！！
```











## 题库

```c++
/********************************************************************/
// c++中的都是从右往左入栈的，在调用函数时，若参数需要运算则先运算，然后入栈，再调用函数。
int AddNums(int a, int b){
    cout << a << " " << b << endl;
    return a + b;
}

int main(){
    /*
    1. 入栈顺序，参数从右往左入栈
    2. 计算顺序，先入栈的先计算；计算完后再入栈
    3. 传递的参数：实际变量，还是临时变量
    */
    int i = 2;
    //1. 先计算，两次i++后i的值为4；传递的是实际变量i的值
    cout << AddNums(++i, ++i) << endl;  // a = 4, b = 4, a + b = 8
    //2. i++入栈的是i，然后执行i++，所以需要临时变量将i的值保存下来，再计算i++；++i先进行计算，入栈为变量i的值
    cout << AddNums(++i, i++) << endl;  // a = 4, b = 2, a + b = 6
    cout << AddNums(i++, ++i) << endl;  // a = 3, b = 4, a + b = 7
    cout << AddNums(i++, i++) << endl;  // a = 3, b = 2, a + b = 5
    cout << AddNums(++i, i) << endl;  // a = 3, b = 3, a + b = 6
}
/********************************************************************/




/********************************************************************/
// 判断条件从左到右。
int main(){
    int x = 1;
    int y = 2;
    if (++x >= 2 || y++ >= 2){ } // ||前半句执行了就结束了
    cout << x << y << endl;  // x = 2, y = 2
}
/********************************************************************/




/********************************************************************/
// 数组指针和指针数组
using Array = int(*)[10]	// 数组指针
typedef int (*Array)[10]	// 数组指针
# typedef int (Array*)[10];	// 申明方式错误！！！  *在变量的左边，类型的右边
    
using Array = int*[10]		// 指针数组
typedef int *Array[10]		// 指针数组
    
    
    
char* p[10];				// 含有10个元素为char*的数组，即指针数组
char (*p)[10];				// 指向char[10]数组的指针
char** p[10];				// 含有10个元素为char**的数组，即含有10个指向char*的指针的数组
char p[10];					// char数组
char* (*p)[10];				// 指向含有10个元素为char*的数组的指针
    
/********************************************************************/




/********************************************************************/
// 不符合编程规范
int a = 10;		// 不能用魔数，应该constexpr int A = 5;


char str[10];
cin.get(str, 5, 'd'); //读取5个字符，并且丢弃'd'字符之后的字符
cout << str; // abcde -> abc   
/********************************************************************/




/********************************************************************/
// 不同类型相加
unsigned int a = 6;
int b = -20;
(a+b > 6) ? (true):(false) // int b 会转成无符号，因此和一定大于6
/********************************************************************/




/********************************************************************/
// 
	int var = 5;
    static int base = 3;
    auto func = [=]() mutable{
        ++base;
        ++var;
        return base + var;
    };
    auto a = func();
    auto b = func();
    cout << a << " " << b << " " << var << " " << base << endl; // 10 12 5 5
/********************************************************************/


/********************************************************************/
	uint32_t i =10;
    cout << i << endl;  // 10
    cout << sizeof(++i) << endl;  // 4
    cout << i << endl;  // 10 sizeof里面的++i没有执行
/********************************************************************/


/********************************************************************/
	int i = 0;
    int j = 0;
    for (i = 10; i >= 0; --i) {
        for (j = 10; j == 1; --j) {
            i = j;
        }
    }
    cout << i << " " << j;  // -1 10
/********************************************************************/
```





























## 面经

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

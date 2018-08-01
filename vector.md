## 模板类vector

- 使用vector对象需要首先#include<vector>
- 要创建vectr模板对象，可使用通常的<type>表示法来指出所要使用的类型。
  vector模板使用动态内存分配，因此可以使用初始化参数指定需要多少矢量。
  
```
#include <vector>
using namespace std;
vector<int> rattings(5);
int n;
cin >> n;
vector<double> scores(n);
```

- 由于运算符[]被重载，因此创建vector对象后，可以使用通常的数组表示法来访问各个元素。

```
rattting[0] = 9;
for(int i=0;i<n;i++)
	cout<<scores[i]<<endl;
```

### 一些容器的方法（包括vector）

- size() -- 返回容器中元素的数目<br/>
- swap() -- 交换两个容器的内容<br/>
- begin() -- 返回一个指向容器中第一个元素的迭代器<br/>
- end() -- 返回指向容器中超过容器尾的迭代器
（超过容器尾就类似原c语言中字符串最后的那个'\0'）<br/>

**\*迭代器类似一个指针**

```
声明一个vector的double类型迭代器
vector<double>::iterator pd;
定义一个scores对象
vector<double> scores;
则可以使用pd进行如下操作：
pd = scores.begin();
*pd = 22.3
pd++;
```

### 一些vector特有方法
- push_back() -- 将元素添加到矢量末尾<br/>
- erase() -- 删除矢量中给定区间的元素。它接收两个迭代器元素，
第一个迭代器指向区间的起始处，第二个指向要删除最后一个元素的后一个位置<br/>

```
// 删除前两个元素
scores.erase(scores.begin(),scores.begin()+2)
```

- insert() -- 将某个向量区间插入指定位置。
接收三个迭代器元素，第一个指定新元素插入位置，第二个和第三个定义需要插入的区间。(第三个迭代器和erase()的第二个一样)

```
// 将new_v中出第一个元素外的所有元素都插入到old_v矢量的第一个元素前
vector<int> old_v;
vecotor<int> new_v;
...
old_v.insert(old_v.begin(),new_v.begin()+1,new_v.end());

// 将new_v中出第一个元素外的所有元素都插入到old_v矢量的最后一个元素后
old_v.insert(old_v.begin(),new_v.begin()+1,new_v.end());

```





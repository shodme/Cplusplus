## ģ����vector

- ʹ��vector������Ҫ����#include<vector>
- Ҫ����vectrģ����󣬿�ʹ��ͨ����<type>��ʾ����ָ����Ҫʹ�õ����͡�
  vectorģ��ʹ�ö�̬�ڴ���䣬��˿���ʹ�ó�ʼ������ָ����Ҫ����ʸ����
  
```
#include <vector>
using namespace std;
vector<int> rattings(5);
int n;
cin >> n;
vector<double> scores(n);
```

- ���������[]�����أ���˴���vector����󣬿���ʹ��ͨ���������ʾ�������ʸ���Ԫ�ء�

```
rattting[0] = 9;
for(int i=0;i<n;i++)
	cout<<scores[i]<<endl;
```

### һЩ�����ķ���������vector��

- size() -- ����������Ԫ�ص���Ŀ<br/>
- swap() -- ������������������<br/>
- begin() -- ����һ��ָ�������е�һ��Ԫ�صĵ�����<br/>
- end() -- ����ָ�������г�������β�ĵ�����
����������β������ԭc�������ַ��������Ǹ�'\0'��<br/>

**\*����������һ��ָ��**

```
����һ��vector��double���͵�����
vector<double>::iterator pd;
����һ��scores����
vector<double> scores;
�����ʹ��pd�������²�����
pd = scores.begin();
*pd = 22.3
pd++;
```

### һЩvector���з���
- push_back() -- ��Ԫ����ӵ�ʸ��ĩβ<br/>
- erase() -- ɾ��ʸ���и��������Ԫ�ء�����������������Ԫ�أ�
��һ��������ָ���������ʼ�����ڶ���ָ��Ҫɾ�����һ��Ԫ�صĺ�һ��λ��<br/>

```
// ɾ��ǰ����Ԫ��
scores.erase(scores.begin(),scores.begin()+2)
```

- insert() -- ��ĳ�������������ָ��λ�á�
��������������Ԫ�أ���һ��ָ����Ԫ�ز���λ�ã��ڶ����͵�����������Ҫ��������䡣(��������������erase()�ĵڶ���һ��)

```
// ��new_v�г���һ��Ԫ���������Ԫ�ض����뵽old_vʸ���ĵ�һ��Ԫ��ǰ
vector<int> old_v;
vecotor<int> new_v;
...
old_v.insert(old_v.begin(),new_v.begin()+1,new_v.end());

// ��new_v�г���һ��Ԫ���������Ԫ�ض����뵽old_vʸ�������һ��Ԫ�غ�
old_v.insert(old_v.begin(),new_v.begin()+1,new_v.end());

```





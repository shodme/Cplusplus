## C/C++�ṹ�嶨��

[�ο�����](http://blog.sina.com.cn/s/blog_4fdabc820100fsxu.html)

- ��c�����У�����һ���ṹ������Ҫ��typdef:

```
typdef struct point{
	int x;
	int y;
}Point;
������������ʱ��Ϳ��ԣ�Point p1;

���û��typdef����
struct point{
	int x;
	int y;
}
������������ʱ��ͱ����ã�struct point p1;

Ҳ����ʡȥpoint,���£�
typdef struct{
	int x;
	int y;
}Point;
```

- ��C++���÷��Ƚϼ�

```
sturct Point{
	int x;
	int y;
};
������һ���ṹ������Point,��������ʱֱ��Point p1;

sturct Point{
	int x;
	int y;
}p1;
// p1��һ���ṹ�����
typdef sturct Point{
	int x;
	int y;
}p2;
// p2 ��һ���ṹ�����ͣ���������ʱp2 p1
```

- ���⣬c�����У�struct���ܰ���������C++�У����԰�������
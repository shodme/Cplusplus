## C/C++结构体定义

[参考博客](http://blog.sina.com.cn/s/blog_4fdabc820100fsxu.html)

- 在c语言中，定义一个结构体类型要用typdef:

```
typdef struct point{
	int x;
	int y;
}Point;
在声明变量的时候就可以：Point p1;

如果没有typdef，如
struct point{
	int x;
	int y;
}
在声明变量的时候就必须用：struct point p1;

也可以省去point,如下：
typdef struct{
	int x;
	int y;
}Point;
```

- 在C++里用法比较简单

```
sturct Point{
	int x;
	int y;
};
定义了一个结构体类型Point,声明变量时直接Point p1;

sturct Point{
	int x;
	int y;
}p1;
// p1是一个结构体变量
typdef sturct Point{
	int x;
	int y;
}p2;
// p2 是一个结构体类型，声明变量时p2 p1
```

- 此外，c语言中，struct不能包含函数；C++中，可以包含函数
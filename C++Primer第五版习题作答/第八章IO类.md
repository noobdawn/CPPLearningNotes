# IO类

## 8.1

```C++
istream& _8_1(istream& in)
{
	char c;
	while (in >> c)
		cout << c;
	in.clear();
	return in;
}
```

## 8.2

无

## 8.3

输入文件终止符或者输入的类型和i的类型不符合出错的时候。

## 8.4

```C++
vector<string> _8_4(string fileName)
{
	ifstream ifs(fileName);
	string s;
	vector<string> ss;
	while (getline(ifs, s))
		ss.push_back(s);
	return ss;
}
```

## 8.5

```C++
vector<string> _8_4(string fileName)
{
	ifstream ifs(fileName);
	string s;
	vector<string> ss;
	while (ifs >> s)
		ss.push_back(s);
	return ss;
}
```

## 8.6

无 

## 8.7

无

## 8.8

无

## 8.9

无

## 8.10

```c++
vector<string> _8_4(string fileName)
{
	ifstream ifs(fileName);
	string s;
	vector<string> ss;
	while (getline(ifs, s))
		ss.push_back(s);
	return ss;
}

int main(int argc, char* argv[]) {
	auto m = _8_4("_8_4.txt");
	for (const auto& str : m)
	{
		istringstream iss(str);
		string word;
		while (iss >> word)
			cout << word << endl;
	}
}
```

## 8.11

```C++
istringstream in;
while(getline(cin, line))
{
    //...
    in.clear();
    in.str(line);
    // ...
}
```

## 8.12

因为电话号码数量不固定

## 8.13

cin换成以下内容的ifs：

```C++
ifstream ifs(fileName);
```

## 8.14

首先，不需要修改，所以是const

其次，防止拷贝赋值，所以是&
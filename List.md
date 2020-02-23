<div
    style = "
        width: 100%;
        height: 50px;
        background: #00FFFF;
        color: black;
        line-height: 50px;
        padding-left: 15px;
        font-size: 24px;
        font-weight: bold;
    "
> 
  List常用属性以及方法
</div>

## 一、List常用属性
1. 通过[] 来访问List中的每一个元素
```dart
  void main() {
    List l = ['a','b','c'];
    print( l[0] ); // 'a'
  }
```
2. List 通过length属性来获得长度
```dart
  void main() {
    List l = ['a','b','c'];
    print( l.length ); // 3
  }
```
3. List通过isEmpty或是isNotEmpty来判断一个List是否为空
```dart
  void main() {
    List l = ['a','b','c'];
    print( l.isEmpty() );  //false
    print( l.isNotEmpty() );  //true
  }
```
4. 翻转数组
```dart
  void main() {
    List l = ['a','b','c'];
    var newList = l.revsered; // ('c','b','a')  
    /* 如果你想将newList转换成List类型，那么可以使用toList方法 */
    print( newList.toList() );// ['c','b','a']
  }
```

## 二、List常用方法
### 添加
1. add
  ```dart
    void main() {
      List list = [ 1,2,3,4 ];
      list.add( '我是西阁' );// 添加单个元素 ,不能添加多个
      print( list ); // [ 1,2,3,4,'我是西阁' ]
    }
  ```
2. addAll
  ```dart
    void main() {
      List list = [ 1,2,3,4 ];
      list.addAll( [5,6] );// 拼接数组
      print( list ); // [ 1,2,3,4,5,6 ]
    }
  ```

### 删除
1. remove...
  ```dart
    void mian() {
      List list = ['🐻','⚽','🎂','🏈','abc','abcd'];
      //删除指定元素
      list.remove("🏈");
      print(list);
      //删除最后一个元素
      list.removeLast();
      print(list);
      //删除指定位置的元素
      list.removeAt(list.length - 1);
      print(list);
      //删除指定区域的元素
      list.removeRange(0,1);
      print(list);
      //下面这个方法是将列表List中的toString之后的字符串的长度等于3的元素全部删除
      list.removeWhere((item) => item.toString().length == 3);
      print("删除列表中toString后长度为3的元素：==> $list");
    }
  ```

### 修改
1. fillRange( startIndex,endIndex,newEle )
```dart
  void main() {
    List list = ['🐻','⚽','🎂','🏈','abc','abcd'];
    list.fillRange( 1,2,'西阁' ); // 在列表下标为1到2之家添加一个字符'西阁'
    print( list );
  }
```
2. insert
```dart
  void main() {
    List list = ['🐻','⚽','🎂','🏈','abc','abcd'];
    list.insert( 1, '西阁') ; // 添加一个
    print( list );
  }
```
3. insertAll( index, [ ele1,ele2,ele3 ])
```dart
  void main() {
    List list = ['🐻','⚽','🎂','🏈','abc','abcd'];
    list.insertAll( 1,['美女','我','能要你个微信吗']);
    print( list );
  }
```

### 查询
1. indexOf()
```dart
  void main() {
    List list = ['🐻','⚽','🎂','🏈','abc','abcd'];
    String str = list.indexOf( 'abc' );
    print( str );// 4    将查找到的元素的下标输出，如果查找不到这个元素，则返回-1
  }
```


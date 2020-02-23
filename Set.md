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
  Set
</div>

## 1. Set是什么？
<div
    style = "background: black;text-align: justify;padding: 10px 8px;letter-spacing: 2px;"
>
    <font color = "greenyellow" style = "font-weight: bold;">  
        Set是没有顺序且不能重复的集合
    </font>
</div>

## 2. Set的作用是什么？
<div
    style = "background: black;text-align: justify;padding: 10px 8px;letter-spacing: 2px;"
>
    <font color = "greenyellow" style = "font-weight: bold;">  
        Set主要作用是去除列表中重复元素
    </font>
</div>

## 3. Set如何使用？
```dart
  void main() {
    var s = new Set();
    List list = ['🐻','⚽','🎂','🏈','abc','abcd','🐻','⚽','🎂','🏈'];
    s.addAll( list );
    print( s ); //{'🐻','⚽','🎂','🏈','abc','abcd'}
  }
```
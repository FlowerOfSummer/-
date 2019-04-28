#### 给定一个计算式（包含加减乘除四则运算）字符串，计算结果
## 算法思想： 
#### 1）将操作数和操作符分别按顺序存放到数组中
        此处我用到的方法是parseInt(str),此函数会返回字符串开头的整数；然后用字符串截取第一个字符sstr.substring(0, 1)就是操作符，两个步骤不能条换顺序
#### 2）遍历操作符数组，先计算优先级较高的\*和/，所以用Array.includes("\*","/")判断是否包含*和/，若有，找到一个，记住当前索引以及操作符就返回；
         记住当前索引既是为了找到当前的操作符，也是为了下一次遍历不从头开始，减小开销
#### 3）计算操作符原本相邻的两个操作数，进行相应的计算，存储单步结果
          将计算过的两个数从数组中删除，将单步结果插入到该位置；操作符同理保证操作数运算顺序不改变，操作符不改变；
#### 4）返回计算最终结果


因为最近在学习vue.js所以这个demo使用vue的相关语法写的，也主要是为了实时展现数据，方便。若大家有更好的方法，或对我的这个算法有建议，欢迎指教哦。qq:1358025287

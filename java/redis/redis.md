1:Redis中string的数据结构
Redis没有使用C中的传统的字符串，而是自己构建了一种名为简单动态字符串（simple dynamic string, sds）的抽象类型，并将sds用作redis的默认字符串表示。

SDS属性
struct sdshdr{
    int len;  // 记录了sds所保留的字符串长度
    int free;  // 记录了buf数组中未使用的字节数量
    char buf[];    字节数组，用于保存字符串。
};

好处：
1：杜绝了缓冲区溢出
2：减少修改字符串是带来的内存重新分配次数
3：二进制安全
4：兼容部分C字符串函数


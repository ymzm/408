
[TOC]

## 6.7 字符串模式匹配
### 6.7.1 简单的模式匹配算法
S为主串 T为模式串
返回值为匹配成功的主串第一个字符下标 返回0代表匹配失败
S[0] T[0] 存放字符串长度； 字符串自下标1开始。
```
int Index (SString S, SString T)
{
    int i=1, j=1;
    while(i<= S[0] && j <= T[0])
    {
        if (S[i] == T[j])
        {
            i++; 
            j++;
        }
        else
        {
            j=1;
            i=i-j+2;
        }
    }
    
    if (j>T[0])
    return i-T[0];
    else
    {
    return 0;
    }
}
```

### 6.7.2 改进的模式匹配算法--KMP算法

```
void get_next(String T, int next[])
{
    int i=1, j=0;
    
    next[1] = 0;
    while(i<T.length)
    {
        if (j==0 || T.ch[i] == T.ch[j])
        {
            
        }
        else
        {
            j=next[j];
        }
    }

}
```

再看王道巩固！
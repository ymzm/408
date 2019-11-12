[ TOC ]

## 图论

** 并查集 **

使用一个数组保存每一个节点的root 没有root则赋值为-1
查找root的root 直至找到root为-1的节点 此节点值为ret
路径上全部节点的root值赋为ret

** 弗洛伊德算法 计算最短路径 **

1) 使用邻接矩阵保存原图
2）原图edge[i][j]为不经过中间节点的ij最短距离
3）i j 可以经过编号小于等于1的节点
4） 。。。
5） 重复N次 edge i j为i j最短距离 

** 迪杰斯特拉算法 单源最短路径 **

1）使用邻接矩阵保存原图 使用dist保存已知最短路径 
2）
3）
4）
5）

##

## map 用法
```
    map<int,int> mp;
    scanf("%d %d", &M, &N);

    for (int i=0; i<M; i++)
    {
        for (int j=0; j<N; j++)
        {
            scanf("%d", &tmp);
            if (mp.find(tmp) != mp.end())
            {
                mp[tmp]++;
            }
            else
            {
                mp[tmp] = 1;
            }
        }
    }
    
```

```
    int k=0; int max=0;
    for (map<int, int>::iterator it = mp.begin(); it != mp.end(); it++)
    {
        if(it->second > max )
        {
            k = it->first;
            max = it->second;
        }
    }
```
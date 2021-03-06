
# 查找算法

* 顺序查找
* 二分查找
* 分块查找
* 动态查找
* 哈希表


## 顺序查找

顺序表查找。复杂度O(n)

## 二分查找

有序表中查找我们可以使用二分查找。

```
/*
eg: [1,3,5,6,7,9] k=6
@return 返回元素的索引下表，找不到就返回-1
*/
int binary_search(int *a,int length,int k){
	int low = 0;
	int high = length-1;
	int mid;

	while(low<high){
		mid = (low+high)/2;
		if (a[mid] < k) low = mid+1;
		if (a[mid == k]) return mid;
		if (a[mid] > k) high = mid-1; 
	}

	return -1;
}
```

## 分块查找

块内无序，块之间有序；可以先二分查找定位到块，然后再到块中顺序查找。


## 动态查找

这里之所以叫 动态查找表，是因为表结构是查找的过程中动态生成的。查找结构通常是二叉排序树，AVL树，B- ，B+等。这部分的内容可以去看『二叉树』章节


## 哈希表

哈希表以复杂度O(1)的成绩位列所有查找算法之首，大量查找的数据结构中都可以看到哈希表的应用。












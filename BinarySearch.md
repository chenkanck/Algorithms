如何发现是二分法

痛点
end condition: `l<r, l<=r, l + 1 < r `

increment `l=mid, l=mid+1, l=mid-1`

Template:
```
while start+1 < end {
    if mid == target {
        end = mid
    } else if mid < target {
        start = mid
    } else {
        end = mid
    }
}
if nums[start] == target {
    return start
}
if nums[end] == target {
    return end
}
return nil
```

#### Level 2: 
找到满足条件的**第一个** 或者**最后一个**位置
#### Level 3:
保留有解的一半
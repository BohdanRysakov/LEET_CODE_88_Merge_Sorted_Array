# Leet Code 88 Merge Sorted Array

## Task level - *Easy*

Actually there is just last part of [Merge Sort](https://en.wikipedia.org/wiki/Merge_sort)

``` Java
if (nums1.length != m + n ||
    nums2.length != n ||
    m < 0 || n > 200 ||
    m + n < 1 ||
    m + n > 200) {
    throw new BadInputException();
    }
    int p1 = m - 1;
    int p2 = n - 1;
    int p = m + n - 1;


    while (p1 >= 0 && p2 >= 0) {
            if (nums1[p1] < nums2[p2]) {
                nums1[p] = nums2[p2];
                p2--;
            } else {
                nums1[p] = nums1[p1];
                p1--;
            }
            p--;
        }
        System.arraycopy(nums2, 0, nums1, 0, p2 + 1);'
```

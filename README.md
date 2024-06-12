### In-place modify list
#### ( Change orginal list for example in class method )

The [:] syntax in Python is a way to modify a list in place, It represents a slice of the entire list, allowing you to assign new values to the list without creating a new list object.
This is particularly useful when you want to ensure that changes are reflected in the original list, especially when working within a method that modifies a list passed as an argument.

```Python
def merge(self, nums1: List[int], m: int, nums2: List[int], n: int) -> None:
        """
        Do not return anything, modify nums1 in-place instead.
        """
        nums1[:] = nums1[:m]
        nums2 = nums2[:n]
        for num in nums2:
            bisect.insort_left(nums1, num)
```

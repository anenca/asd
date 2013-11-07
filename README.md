quicksort

```c
Hoare-Partition(A, p, r)
x = A[p]
i = p - 1
j = r + 1
while true
    repeat
        j = j - 1
    until A[j] <= x
    repeat
        i = i + 1
    until A[i] >= x
    if i < j
        swap( A[i], A[j] )
    else
        return j
```
and:
```c
Lomuto-Partition(A, p, r)
x = A[r]
i = p - 1
for j = p to r - 1
    if A[j] <= x
        i = i + 1
        swap( A[i], A[j] )
swap( A[i +1], A[r] )
return i + 1

```
```c
Quicksort(A,p,r){
if (p<r)
  then{ q = Partition(A,p,r)
    Quicksort(A,p, q-1)
    Quicksort(A,q+1,r)
  }
}
```

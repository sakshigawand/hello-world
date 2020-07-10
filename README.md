# searching a number in an array
array =list([1,2,3,4,5])
find =int(input("enter the number to be searched = "))


def binary_search(array, low, high):
    if low < high:
        mid = (low + high) // 2
        if find < array[mid]:
            return binary_search(array, low, mid)
        elif find > array[mid]:
            return binary_search(array, mid+1, high)
        else:
            return mid
    return -1


index = binary_search(array, 0, len(array))
print(index)

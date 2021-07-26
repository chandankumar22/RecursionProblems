class Solution {
    fun sortArray(nums: IntArray): IntArray {
        //if(nums.size<2) return nums
        return sort(nums.toMutableList() as ArrayList<Int>).toIntArray()
    }
    
    fun sort(arr:ArrayList<Int>):ArrayList<Int>{
        println("sort called on ${arr.toList()}")
        if(arr.size==1){
                 println("return sorted arr ${arr.toList()}")
         return arr   
        }
        val elementToInsertAfterSort = arr[arr.size-1]
           println("element to insert after sort $elementToInsertAfterSort")
        arr.removeAt(arr.size-1)
        val sortedArray = sort(arr)
        return insert(sortedArray,elementToInsertAfterSort)
    }
    
    fun insert(arr:ArrayList<Int>,element:Int):ArrayList<Int>{
         println("insert called on ${arr.toList()} and element to insert $element")
        if(arr.isEmpty() || arr[arr.size-1]<=element){
            arr.add(element)
             println("insert returning ${arr.toList()}")
            return arr
        }
        val lastEl = arr[arr.size-1]
        arr.removeAt(arr.size-1)
        val insArr = insert(arr,element)
        insArr.add(lastEl)
        return insArr
    }
    
}

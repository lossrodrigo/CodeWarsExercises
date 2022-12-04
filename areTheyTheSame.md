#### Are they the "same"?

##### https://www.codewars.com/kata/550498447451fbbd7600041c/train/kotlin

#### **Solution**

fun comp(a: IntArray?, b: IntArray?): Boolean {
    val a = intArrayOf(1, 2, 3)
    val b = intArrayOf(1, 4, 9)
    var result = false

    if(a !== null && b !== null && a.indices == b.indices) {
        val aSquare = mutableSetOf<Int>()
    
        for (i in a.indices){
            aSquare.add(a[i]*a[i])
        }
    
        if (b.toSet() == aSquare) {
            result = true
        }
    
    }

  return result
}
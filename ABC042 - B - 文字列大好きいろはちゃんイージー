
```kotlin

fun main() {
    val (n, _) = readLine()!!.split(" ").map { it.toInt() }
    val list = mutableListOf<String>()
    for (i in 1..n) list.add(readLine()!!)
    println(bubbleSort(n, list).joinToString(""))
}
 
fun <T> MutableList<T>.swap(index1: Int, index2: Int) {
    val tmp = this[index1]
    this[index1] = this[index2]
    this[index2] = tmp
}
 
fun bubbleSort(listSize: Int, list: MutableList<String>): List<String> {
    var head = 0
    while (head < listSize - 1) {
        for (j in listSize - 1 downTo head + 1) {
            if (list[j] < list[j - 1]) {
                list.swap(j, j - 1) // list[j]とlist[j - 1]の入れ替え
            }
        }
        head ++
    }
    return list
}
```

```kotlin
fun main() {
    readLine()!!
    val intList = readLine()!!.split(" ").map { it.toInt() }
    val costList = mutableListOf<Int>()
    val average = intList.sum() / intList.size
    var sum = 0
    for (i in intList) {
        sum += (i - average) * (i - average)
    }
    costList.add(sum)
    sum = 0
    for (i in intList) {
        sum += (i - average - 1) * (i - average - 1)
    }
    costList.add(sum)
    println(costList.min())
 
}
```

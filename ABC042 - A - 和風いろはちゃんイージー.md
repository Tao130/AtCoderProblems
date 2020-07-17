``` answer.kt
fun main() {
    val list = readLine()!!.split(" ").map { it.toInt() }
    var fiveCount = 0
    var sevenCount = 0
    for (i in list) {
        if (i == 5) fiveCount++
        if (i == 7) sevenCount++
    }
    if (fiveCount == 2 && sevenCount == 1) println("YES") else println("NO")
}
```

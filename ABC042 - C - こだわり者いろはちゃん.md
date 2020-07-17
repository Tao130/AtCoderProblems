```kotlin
fun main() {
    var (n, k) = readLine()!!.split(" ").map { it.toInt() }
    val dislikeList = readLine()!!.split(" ")
    var canPurchase = false
    while (!canPurchase) {
        var count = 0
        for (i in 0 until k) {
            if (n.toString().contains(dislikeList[i])) {
                count++
            }
        }
        if (count == 0) {
            canPurchase = true
        }
        n++
    }
    println(n - 1)
}
```

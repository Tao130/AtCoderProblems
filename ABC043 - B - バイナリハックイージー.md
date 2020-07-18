```kotlin
fun main() {
    val s = readLine()!!
    val answerList = mutableListOf<String>()
    loop@ for (i in s.indices) {
        when (s.substring(i, i + 1)) {
            "0" -> answerList.add("0")
            "1" -> answerList.add("1")
            else -> if (answerList.size == 0) {
                continue@loop
            } else {
                answerList.removeAt(answerList.size - 1)
            }
        }
    }
    println(answerList.joinToString(""))
}
```

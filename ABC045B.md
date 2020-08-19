```ABC045.kt
fun main() {
    var aList = readLine()!!.toCharArray().toMutableList()
    var bList = readLine()!!.toCharArray().toMutableList()
    var cList = readLine()!!.toCharArray().toMutableList()
    var nextPlayer = 'a'

    loop@ while (true) {
        when (nextPlayer) {
            'a' -> {
                if (aList.size == 0) break@loop
                nextPlayer = aList[0]
                aList = aList.drop(1).toMutableList()
            }
            'b' -> {
                if (bList.size == 0) break@loop
                nextPlayer = bList[0]
                bList = bList.drop(1).toMutableList()
            }
            'c' -> {
                if (cList.size == 0) break@loop
                nextPlayer = cList[0]
                cList = cList.drop(1).toMutableList()
            }
        }


    }

    println(
            when (nextPlayer) {
                'a' -> "A"
                'b' -> "B"
                else -> "C"
            }
    )
}
```

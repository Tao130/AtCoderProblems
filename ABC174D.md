``` answer.kt
fun main() {
    readLine()!!.toInt()
    val list: MutableList<String> = readLine()!!.split("").filter { it != "" } as MutableList<String>
    var flagForward = 0
    var flagBack = list.size - 1
    var count = 0
    loop@ while (true) {
        if (flagBack <= flagForward ) break
        if (list[flagForward] == "R") {
            flagForward++
        } else {
            while (list[flagBack] != "R") {
                flagBack--
                if (flagForward == flagBack) break@loop
            }
            list[flagForward] = "R"
            list[flagBack] = "W"
            count++
            flagForward++
            flagBack--
        }
    }
    println(count)
}
```

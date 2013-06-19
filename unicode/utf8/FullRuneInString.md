
## func FullRuneInString(s string) bool

参数列表

- p 目标字符串


返回值：

- bool  是否是完整的UTF-8字节

功能说明：

这个函数主要是用来判断字符串中第一个字节是不是完整的UTF-8字节

代码实例：

package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	str := "世"
	fmt.Println(utf8.FullRuneInString(str))
	fmt.Println(utf8.FullRuneInString(str[:2]))
}



输出:
true
false
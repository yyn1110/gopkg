
## func FullRune(p []byte) bool

参数列表

- p 目标字节数组


返回值：

- bool  是否是完整的UTF-8字节

功能说明：

这个函数主要是用来判断第一个字节是不是完整的UTF-8字节

代码实例：

package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	buf := []byte{228, 184, 150} // 世
	fmt.Println(utf8.FullRune(buf))
	fmt.Println(utf8.FullRune(buf[:2]))

}


输出:
true
false
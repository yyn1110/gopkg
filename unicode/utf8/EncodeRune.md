
## func EncodeRune(p []byte, r rune) int

参数列表

- p 将要写入字节的目标字节数组
- r 将要写入的字节

返回值：

- int  返回写入的字节的宽度

功能说明：

这个函数主要是用来将一个字节写入一个字节数组，注意：字节数组空间必须足够大

代码实例：

package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	r := '世'
	buf := make([]byte, 3)

	n := utf8.EncodeRune(buf, r)

	fmt.Println(buf)
	fmt.Println(n)

}

输出:
[228 184 150]
3
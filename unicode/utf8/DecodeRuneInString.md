
## func DecodeRuneInString(s string) (r rune, size int)

参数列表

- s 表示目标字符串

返回值：

- r    第一个字节的UTF-8码
- size 返回第一个字节的宽度

功能说明：

这个函数主要是用来获得字符串中的第一个字节转换为UTF-8码，如果不能正确转换则返回(RuneError, 1)

代码实例：

package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	p := "A hello"
	r, size := utf8.DecodeRuneInString(p)
	if r != utf8.RuneError {
		fmt.Println(r, size)
	} else {
		fmt.Println(utf8.RuneError, size)

	}
}
输出:
H 1
e 1
l 1
l 1
o 1
, 1
  1
世 3
界 3
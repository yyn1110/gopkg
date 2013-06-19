
## func DecodeRune(p []byte) (r rune, size int)

参数列表

- p 表示目标字节数组

返回值：

- r    第一个字节的UTF-8码
- size 返回第一个字节的宽度

功能说明：

这个函数主要是用来获得字节数组中的第一个字节转换为UTF-8码，如果不能正确转换则返回(RuneError, 1)

代码实例：

package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	b := []byte("Hello, 世界")

	for len(b) > 0 {
		r, size := utf8.DecodeRune(b)
		fmt.Printf("%c %v\n", r, size)

		b = b[size:]
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
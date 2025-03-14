---
title: ASCII码表
published: 2025-03-14
description: ''
image: ''
tags: []
category: 'c语言'
draft: false 
lang: ''
---



# ASCII编码表

American Standard Code for Information Interchange；美国信息交换标准代码

ASCII是基于拉丁字母的一套电脑编码系统，主要用于显示现代英语和其他西欧语言。它是最通用的信息交换标准，并等同于国际标准ISO/IEC 646。ASCII第一次以规范标准的类型发表是在1967年，最后一次更新则是在1986年，ASCII 码的十进制范围为 [0-255]，包括 [0-31] 为控制字符或通信专用字符，[32-127] 为可打印字符，[128-255] 为扩展的 ASCII 码。

## ASCII 控制字符 (字符码 0-31)

ASCII 表中的前 32 个字符是不可打印的控制代码，用于控制外围设备，例如打印机。


| DEC 十进制 | OCT 八进制 | HEX 十六进制 | BIN 二进制 | Symbol | HTML Number | HTML Name | Description                  | 中文描述     |
| :--------- | :--------- | :----------- | :--------- | :----- | :---------- | :-------- | :--------------------------- | :----------- |
| 0          | 00         | 0x00         | 00000000   | NUL    | \&#000;     |           | Nullchar                     | 空字符       |
| 1          | 01         | 0x01         | 00000001   | SOH    | \&#001;     |           | Start of Heading             | 标题开始     |
| 2          | 02         | 0x02         | 00000010   | STX    | \&#002;     |           | Start of Text                | 正文开始     |
| 3          | 03         | 0x03         | 00000011   | ETX    | \&#003;     |           | End of Text                  | 正文结束     |
| 4          | 04         | 0x04         | 00000100   | EOT    | \&#004;     |           | End of Transmission          | 传输结束     |
| 5          | 05         | 0x05         | 00000101   | ENQ    | \&#005;     |           | Enquiry                      | 查询         |
| 6          | 06         | 0x06         | 00000110   | ACK    | \&#006;     |           | Acknowledgment               | 确认         |
| 7          | 07         | 0x07         | 00000111   | BEL    | \&#007;     |           | Bell                         | 振铃         |
| 8          | 010        | 0x08         | 00001000   | BS     | \&#008;     |           | Back Space                   | 退格         |
| 9          | 011        | 0x09         | 00001001   | HT     | \&#009;     |           | Horizontal Tab               | 水平制表符   |
| 10         | 012        | 0x0A         | 00001010   | LF     | \&#010;     |           | Line Feed , \n               | 换行键       |
| 11         | 013        | 0x0B         | 00001011   | VT     | \&#011;     |           | Vertical Tab                 | 垂直制表符   |
| 12         | 014        | 0x0C         | 00001100   | FF     | \&#012;     |           | Form Feed                    | 换页键       |
| 13         | 015        | 0x0D         | 00001101   | CR     | \&#013;     |           | Carriage Return , \r         | 回车键       |
| 14         | 016        | 0x0E         | 00001110   | SO     | \&#014;     |           | Shift Out / X-On             | 移出         |
| 15         | 017        | 0x0F         | 00001111   | SI     | \&#015;     |           | ShiftIn/X-Off                | 移入         |
| 16         | 020        | 0x10         | 00010000   | DLE    | \&#016;     |           | Data Line Escape             | 数据链路转义 |
| 17         | 021        | 0x11         | 00010001   | DC1    | \&#017;     |           | Device Control 1 (oft. XON)  | 设备控制 1   |
| 18         | 022        | 0x12         | 00010010   | DC2    | \&#018;     |           | Device Control 2             | 设备控制 2   |
| 19         | 023        | 0x13         | 00010011   | DC3    | \&#019;     |           | Device Control 3 (oft. XOFF) | 设备控制 3   |
| 20         | 024        | 0x14         | 00010100   | DC4    | \&#020;     |           | Device Control 4             | 设备控制 4   |
| 21         | 025        | 0x15         | 00010101   | NAK    | \&#021;     |           | Negative Acknowledgement     | 反确认       |
| 22         | 026        | 0x16         | 00010110   | SYN    | \&#022;     |           | Synchronous Idle             | 同步空闲     |
| 23         | 027        | 0x17         | 00010111   | ETB    | \&#023;     |           | End of Transmit Block        | 传输块结束   |
| 24         | 030        | 0x18         | 00011000   | CAN    | \&#024;     |           | Cancel                       | 取消         |
| 25         | 031        | 0x19         | 00011001   | EM     | \&#025;     |           | End of Medium                | 介质中断     |
| 26         | 032        | 0x1A         | 00011010   | SUB    | \&#026;     |           | Substitute                   | 替换         |
| 27         | 033        | 0x1B         | 00011011   | ESC    | \&#027;     |           | Escape                       | 转义         |
| 28         | 034        | 0x1C         | 00011100   | FS     | \&#028;     |           | File Separator               | 文件分隔符   |
| 29         | 035        | 0x1D         | 00011101   | GS     | \&#029;     |           | Group Separator              | 组分隔符     |
| 30         | 036        | 0x1E         | 00011110   | RS     | \&#030;     |           | Record Separator             | 记录分离符   |
| 31         | 037        | 0x1F         | 00011111   | US     | \&#031;     |           | Unit Separator               | 单元分隔符   |

## ASCII 可打印字符（字符码 32-127）

字符码 32-127 对于 ASCII 表的所有不同变体都是通用的，它们被称为可打印字符，代表字母、数字、标点符号和一些杂项符号。 您几乎可以在 键盘 上找到每个字符，例如字符 127 表示命令 DEL。

| DEC 十进制 | OCT 八进制 | HEX 十六进制 | BIN 二进制 | Symbol | HTML Number | HTML Name | Description                            | 中文描述     |
| :--------- | :--------- | :----------- | :--------- | :----- | :---------- | :-------- | :------------------------------------- | :----------- |
| 32         | 040        | 0x20         | 00100000   |        | \&#32;      |           | Space                                  | 空格         |
| 33         | 041        | 0x21         | 00100001   | !      | \&#33;      |           | Exclamation mark                       | 感叹号       |
| 34         | 042        | 0x22         | 00100010   | "      | \&#34;      | \&quot;   | Double quotes (or speech marks)        | 双引号       |
| 35         | 043        | 0x23         | 00100011   | #      | \&#35;      |           | Number                                 | 井号         |
| 36         | 044        | 0x24         | 00100100   | $      | \&#36;      |           | Dollar                                 | 美元符       |
| 37         | 045        | 0x25         | 00100101   | %      | \&#37;      |           | Per cent sign                          | 百分号       |
| 38         | 046        | 0x26         | 00100110   | &      | \&#38;      | \&amp;    | Ampersand                              | 与           |
| 39         | 047        | 0x27         | 00100111   | '      | \&#39;      |           | Single quote                           | 单引号       |
| 40         | 050        | 0x28         | 00101000   | (      | \&#40;      |           | Open parenthesis (or open bracket)     | 左括号       |
| 41         | 051        | 0x29         | 00101001   | )      | \&#41;      |           | Close parenthesis (or close bracket)   | 右括号       |
| 42         | 052        | 0x2A         | 00101010   | *      | \&#42;      |           | Asterisk                               | 星号         |
| 43         | 053        | 0x2B         | 00101011   | +      | \&#43;      |           | Plus                                   | 加号         |
| 44         | 054        | 0x2C         | 00101100   | ,      | \&#44;      |           | Comma                                  | 逗号         |
| 45         | 055        | 0x2D         | 00101101   | -      | \&#45;      |           | Hyphen                                 | 连字号或减号 |
| 46         | 056        | 0x2E         | 00101110   | .      | \&#46;      |           | Period, dot or full stop               | 句点或小数点 |
| 47         | 057        | 0x2F         | 00101111   | /      | \&#47;      |           | Slash or divide                        | 斜杠         |
| 48         | 060        | 0x30         | 00110000   | 0      | \&#48;      |           | Zero                                   | 0            |
| 49         | 061        | 0x31         | 00110001   | 1      | \&#49;      |           | One                                    | 1            |
| 50         | 062        | 0x32         | 00110010   | 2      | \&#50;      |           | Two                                    | 2            |
| 51         | 063        | 0x33         | 00110011   | 3      | \&#51;      |           | Three                                  | 3            |
| 52         | 064        | 0x34         | 00110100   | 4      | \&#52;      |           | Four                                   | 4            |
| 53         | 065        | 0x35         | 00110101   | 5      | \&#53;      |           | Five                                   | 5            |
| 54         | 066        | 0x36         | 00110110   | 6      | \&#54;      |           | Six                                    | 6            |
| 55         | 067        | 0x37         | 00110111   | 7      | \&#55;      |           | Seven                                  | 7            |
| 56         | 070        | 0x38         | 00111000   | 8      | \&#56;      |           | Eight                                  | 8            |
| 57         | 071        | 0x39         | 00111001   | 9      | \&#57;      |           | Nine                                   | 9            |
| 58         | 072        | 0x3A         | 00111010   | :      | \&#58;      |           | Colon                                  | 冒号         |
| 59         | 073        | 0x3B         | 00111011   | ;      | \&#59;      |           | Semicolon                              | 分号         |
| 60         | 074        | 0x3C         | 00111100   | <      | \&#60;      | \&lt;     | Less than (or open angled bracket)     | 小于         |
| 61         | 075        | 0x3D         | 00111101   | =      | \&#61;      |           | Equals                                 | 等号         |
| 62         | 076        | 0x3E         | 00111110   | >      | \&#62;      | \&gt;     | Greater than (or close angled bracket) | 大于         |
| 63         | 077        | 0x3F         | 00111111   | ?      | \&#63;      |           | Question mark                          | 问号         |
| 64         | 0100       | 0x40         | 01000000   | @      | \&#64;      |           | At symbol                              | 电子邮件符号 |
| 65         | 0101       | 0x41         | 01000001   | A      | \&#65;      |           | Uppercase A                            | 大写字母 A   |
| 66         | 0102       | 0x42         | 01000010   | B      | \&#66;      |           | Uppercase B                            | 大写字母 B   |
| 67         | 0103       | 0x43         | 01000011   | C      | \&#67;      |           | Uppercase C                            | 大写字母 C   |
| 68         | 0104       | 0x44         | 01000100   | D      | \&#68;      |           | Uppercase D                            | 大写字母 D   |
| 69         | 0105       | 0x45         | 01000101   | E      | \&#69;      |           | Uppercase E                            | 大写字母 E   |
| 70         | 0106       | 0x46         | 01000110   | F      | \&#70;      |           | Uppercase F                            | 大写字母 F   |
| 71         | 0107       | 0x47         | 01000111   | G      | \&#71;      |           | Uppercase G                            | 大写字母 G   |
| 72         | 0110       | 0x48         | 01001000   | H      | \&#72;      |           | Uppercase H                            | 大写字母 H   |
| 73         | 0111       | 0x49         | 01001001   | I      | \&#73;      |           | Uppercase I                            | 大写字母 I   |
| 74         | 0112       | 0x4A         | 01001010   | J      | \&#74;      |           | Uppercase J                            | 大写字母 J   |
| 75         | 0113       | 0x4B         | 01001011   | K      | \&#75;      |           | Uppercase K                            | 大写字母 K   |
| 76         | 0114       | 0x4C         | 01001100   | L      | \&#76;      |           | Uppercase L                            | 大写字母 L   |
| 77         | 0115       | 0x4D         | 01001101   | M      | \&#77;      |           | Uppercase M                            | 大写字母 M   |
| 78         | 0116       | 0x4E         | 01001110   | N      | \&#78;      |           | Uppercase N                            | 大写字母 N   |
| 79         | 0117       | 0x4F         | 01001111   | O      | \&#79;      |           | Uppercase O                            | 大写字母 O   |
| 80         | 0120       | 0x50         | 01010000   | P      | \&#80;      |           | Uppercase P                            | 大写字母 P   |
| 81         | 0121       | 0x51         | 01010001   | Q      | \&#81;      |           | Uppercase Q                            | 大写字母 Q   |
| 82         | 0122       | 0x52         | 01010010   | R      | \&#82;      |           | Uppercase R                            | 大写字母 R   |
| 83         | 0123       | 0x53         | 01010011   | S      | \&#83;      |           | Uppercase S                            | 大写字母 S   |
| 84         | 0124       | 0x54         | 01010100   | T      | \&#84;      |           | Uppercase T                            | 大写字母 T   |
| 85         | 0125       | 0x55         | 01010101   | U      | \&#85;      |           | Uppercase U                            | 大写字母 U   |
| 86         | 0126       | 0x56         | 01010110   | V      | \&#86;      |           | Uppercase V                            | 大写字母 V   |
| 87         | 0127       | 0x57         | 01010111   | W      | \&#87;      |           | Uppercase W                            | 大写字母 W   |
| 88         | 0130       | 0x58         | 01011000   | X      | \&#88;      |           | Uppercase X                            | 大写字母 X   |
| 89         | 0131       | 0x59         | 01011001   | Y      | \&#89;      |           | Uppercase Y                            | 大写字母 Y   |
| 90         | 0132       | 0x5A         | 01011010   | Z      | \&#90;      |           | Uppercase Z                            | 大写字母 Z   |
| 91         | 0133       | 0x5B         | 01011011   | [      | \&#91;      |           | Opening bracket                        | 左中括号     |
| 92         | 0134       | 0x5C         | 01011100   | \      | \&#92;      |           | Backslash                              | 反斜杠       |
| 93         | 0135       | 0x5D         | 01011101   | ]      | \&#93;      |           | Closing bracket                        | 右中括号     |
| 94         | 0136       | 0x5E         | 01011110   | ^      | \&#94;      |           | Caret - circumflex                     | 音调符号     |
| 95         | 0137       | 0x5F         | 01011111   | _      | \&#95;      |           | Underscore                             | 下划线       |
| 96         | 0140       | 0x60         | 01100000   | `      | \&#96;      |           | Grave accent                           | 重音符       |
| 97         | 0141       | 0x61         | 01100001   | a      | \&#97;      |           | Lowercase a                            | 小写字母 a   |
| 98         | 0142       | 0x62         | 01100010   | b      | \&#98;      |           | Lowercase b                            | 小写字母 b   |
| 99         | 0143       | 0x63         | 01100011   | c      | \&#99;      |           | Lowercase c                            | 小写字母 c   |
| 100        | 0144       | 0x64         | 01100100   | d      | \&#100;     |           | Lowercase d                            | 小写字母 d   |
| 101        | 0145       | 0x65         | 01100101   | e      | \&#101;     |           | Lowercase e                            | 小写字母 e   |
| 102        | 0146       | 0x66         | 01100110   | f      | \&#102;     |           | Lowercase f                            | 小写字母 f   |
| 103        | 0147       | 0x67         | 01100111   | g      | \&#103;     |           | Lowercase g                            | 小写字母 g   |
| 104        | 0150       | 0x68         | 01101000   | h      | \&#104;     |           | Lowercase h                            | 小写字母 h   |
| 105        | 0151       | 0x69         | 01101001   | i      | \&#105;     |           | Lowercase i                            | 小写字母 i   |
| 106        | 0152       | 0x6A         | 01101010   | j      | \&#106;     |           | Lowercase j                            | 小写字母 j   |
| 107        | 0153       | 0x6B         | 01101011   | k      | \&#107;     |           | Lowercase k                            | 小写字母 k   |
| 108        | 0154       | 0x6C         | 01101100   | l      | \&#108;     |           | Lowercase l                            | 小写字母 l   |
| 109        | 0155       | 0x6D         | 01101101   | m      | \&#109;     |           | Lowercase m                            | 小写字母 m   |
| 110        | 0156       | 0x6E         | 01101110   | n      | \&#110;     |           | Lowercase n                            | 小写字母 n   |
| 111        | 0157       | 0x6F         | 01101111   | o      | \&#111;     |           | Lowercase o                            | 小写字母 o   |
| 112        | 0160       | 0x70         | 01110000   | p      | \&#112;     |           | Lowercase p                            | 小写字母 p   |
| 113        | 0161       | 0x71         | 01110001   | q      | \&#113;     |           | Lowercase q                            | 小写字母 q   |
| 114        | 0162       | 0x72         | 01110010   | r      | \&#114;     |           | Lowercase r                            | 小写字母 r   |
| 115        | 0163       | 0x73         | 01110011   | s      | \&#115;     |           | Lowercase s                            | 小写字母 s   |
| 116        | 0164       | 0x74         | 01110100   | t      | \&#116;     |           | Lowercase t                            | 小写字母 t   |
| 117        | 0165       | 0x75         | 01110101   | u      | \&#117;     |           | Lowercase u                            | 小写字母 u   |
| 118        | 0166       | 0x76         | 01110110   | v      | \&#118;     |           | Lowercase v                            | 小写字母 v   |
| 119        | 0167       | 0x77         | 01110111   | w      | \&#119;     |           | Lowercase w                            | 小写字母 w   |
| 120        | 0170       | 0x78         | 01111000   | x      | \&#120;     |           | Lowercase x                            | 小写字母 x   |
| 121        | 0171       | 0x79         | 01111001   | y      | \&#121;     |           | Lowercase y                            | 小写字母 y   |
| 122        | 0172       | 0x7A         | 01111010   | z      | \&#122;     |           | Lowercase z                            | 小写字母 z   |
| 123        | 0173       | 0x7B         | 01111011   | {      | \&#123;     |           | Opening brace                          | 左大括号     |
| 124        | 0174       | 0x7C         | 01111100   | \|     | \&#124;     |           | Vertical bar                           | 垂直线       |
| 125        | 0175       | 0x7D         | 01111101   | }      | \&#125;     |           | Closing brace                          | 右大括号     |
| 126        | 0176       | 0x7E         | 01111110   | ~      | \&#126;     |           | Equivalency sign - tilde               | 波浪号       |
| 127        | 0177       | 0x7F         | 01111111   |        | \&#127;     |           | Delete                                 | 删除         |

## 扩展的 ASCII 码（字符码 128-255）

8 位 ASCII 表有几种不同的变体。下表是根据 Windows-1252 (CP-1252)，在可打印字符方面，它是 ISO 8859-1（也称为 ISO Latin-1）的超集， 但与 IANA 的 ISO-8859-1 不同的是使用了 displayable 字符而不是 128 到 159 范围内的控制字符。 与 ISO-8859-1 不同的字符用浅蓝色标记。

| DEC 十进制 | OCT 八进制 | HEX 十六进制 | BIN 二进制 | Symbol | HTML Number | HTML Name | Description                                | 中文描述                           |
| :--------- | :--------- | :----------- | :--------- | :----- | :---------- | :-------- | :----------------------------------------- | :--------------------------------- |
| 128        | 0200       | 0x80         | 10000000   | €      | \&#128;     | &euro;    | Euro sign                                  | 欧盟符号                           |
| 129        | 0201       | 0x81         | 10000001   |        |             |           |                                            |                                    |
| 130        | 0202       | 0x82         | 10000010   | ‚      | \&#130;     | \&sbquo;  | Single low-9 quotation mark                | 单低 9 引号                        |
| 131        | 0203       | 0x83         | 10000011   | ƒ      | \&#131;     | \&fnof;   | Latin small letter f with hook             | 带钩的 拉丁小写字母f               |
| 132        | 0204       | 0x84         | 10000100   | „      | \&#132;     | \&bdquo;  | Double low-9 quotation mark                | 双低 9 引号                        |
| 133        | 0205       | 0x85         | 10000101   | …      | \&#133;     | \&hellip; | Horizontal ellipsis                        | 水平省略号                         |
| 134        | 0206       | 0x86         | 10000110   | †      | \&#134;     | \&dagger; | Dagger                                     | 剑号                               |
| 135        | 0207       | 0x87         | 10000111   | ‡      | \&#135;     | \&Dagger; | Double dagger                              | 双剑号                             |
| 136        | 0210       | 0x88         | 10001000   | ˆ      | \&#136;     | \&circ;   | Modifier letter circumflex accent          | 修正字符 抑扬音符号                |
| 137        | 0211       | 0x89         | 10001001   | ‰      | \&#137;     | \&permil; | Per mille sign                             | 千分号                             |
| 138        | 0212       | 0x8A         | 10001010   | Š      | \&#138;     | \&Scaron; | Latin capital letter S with caron          | 带弯音号的 拉丁大写字母 S          |
| 139        | 0213       | 0x8B         | 10001011   | ‹      | \&#139;     | \&lsaquo; | Single left-pointing angle quotation       | 左单书名号                         |
| 140        | 0214       | 0x8C         | 10001100   | Œ      | \&#140;     | \&OElig;  | Latin capital ligature OE                  | 拉丁大写组合 OE                    |
| 141        | 0215       | 0x8D         | 10001101   |        |             |           |                                            |                                    |
| 142        | 0216       | 0x8E         | 10001110   | Ž      | \&#142;     |           | Latin capital letter Z with caron          | 带弯音号的 拉丁大写字母 z          |
| 143        | 0217       | 0x8F         | 10001111   |        |             |           |                                            |                                    |
| 144        | 0220       | 0x90         | 10010000   |        |             |           |                                            |                                    |
| 145        | 0221       | 0x91         | 10010001   | ‘      | \&#145;     | \&lsquo;  | Left single quotation mark                 | 左单引号                           |
| 146        | 0222       | 0x92         | 10010010   | ’      | \&#146;     | \&rsquo;  | Right single quotation mark                | 右单引号                           |
| 147        | 0223       | 0x93         | 10010011   | “      | \&#147;     | \&ldquo;  | Left double quotation mark                 | 左双引号                           |
| 148        | 0224       | 0x94         | 10010100   | ”      | \&#148;     | \&rdquo;  | Right double quotation mark                | 右双引号                           |
| 149        | 0225       | 0x95         | 10010101   | •      | \&#149;     | \&bull;   | Bullet                                     |                                    |
| 150        | 0226       | 0x96         | 10010110   | –      | \&#150;     | \&ndash;  | En dash                                    | 半长破折号                         |
| 151        | 0227       | 0x97         | 10010111   | —      | \&#151;     | \&mdash;  | Em dash                                    | 全长破折号                         |
| 152        | 0230       | 0x98         | 10011000   | ˜      | \&#152;     | \&tilde;  | Small tilde                                | 小波浪线                           |
| 153        | 0231       | 0x99         | 10011001   | ™      | \&#153;     | \&trade;  | Trade mark sign                            |                                    |
| 154        | 0232       | 0x9A         | 10011010   | š      | \&#154;     | \&scaron; | Latin small letter S with caron            | 带弯音号的 拉丁小写字母 s          |
| 155        | 0233       | 0x9B         | 10011011   | ›      | \&#155;     | \&rsaquo; | Single right-pointing angle quotation mark | 右单书名号                         |
| 156        | 0234       | 0x9C         | 10011100   | œ      | \&#156;     | \&oelig;  | Latin small ligature oe                    | 拉丁小写组合 oe                    |
| 157        | 0235       | 0x9D         | 10011101   |        |             |           |                                            |                                    |
| 158        | 0236       | 0x9E         | 10011110   | ž      | \&#158;     |           | Latin small letter z with caron            | 带弯音号的 拉丁小写字母 z          |
| 159        | 0237       | 0x9F         | 10011111   | Ÿ      | \&#159;     | \&Yuml;   | Latin capital letter Y with diaeresis      | 带弯音号的 拉丁大写字母 Y          |
| 160        | 0240       | 0xA0         | 10100000   |        | \&#160;     | \&nbsp;   | Non-breaking space                         |                                    |
| 161        | 0241       | 0xA1         | 10100001   | ¡      | \&#161;     | \&iexcl;  | Inverted exclamation mark                  | 反向感叹号                         |
| 162        | 0242       | 0xA2         | 10100010   | ¢      | \&#162;     | \&cent;   | Cent sign                                  | 分币符号                           |
| 163        | 0243       | 0xA3         | 10100011   | £      | \&#163;     | \&pound;  | Pound sign                                 | 英磅符号                           |
| 164        | 0244       | 0xA4         | 10100100   | ¤      | \&#164;     | \&curren; | Currency sign                              |                                    |
| 165        | 0245       | 0xA5         | 10100101   | ¥      | \&#165;     | \&yen;    | Yen sign                                   | 人民币符号                         |
| 166        | 0246       | 0xA6         | 10100110   | ¦      | \&#166;     | \&brvbar; | Pipe, Broken vertical bar                  |                                    |
| 167        | 0247       | 0xA7         | 10100111   | §      | \&#167;     | \&sect;   | Section sign                               | 章节符号                           |
| 168        | 0250       | 0xA8         | 10101000   | ¨      | \&#168;     | \&uml;    | Spacing diaeresis - umlaut                 | 通用货币符号                       |
| 169        | 0251       | 0xA9         | 10101001   | ©      | \&#169;     | \&copy;   | Copyright sign                             | 版权符号                           |
| 170        | 0252       | 0xAA         | 10101010   | ª      | \&#170;     | \&ordf;   | Feminine ordinal indicator                 | 阴性顺序 指示符号                  |
| 171        | 0253       | 0xAB         | 10101011   | «      | \&#171;     | \&laquo;  | Left double angle quotes                   | 左角引号                           |
| 172        | 0254       | 0xAC         | 10101100   | ¬      | \&#172;     | \&not;    | Not sign                                   |                                    |
| 173        | 0255       | 0xAD         | 10101101   | ­      | \&#173;     | \&shy;    | Soft hyphen                                |                                    |
| 174        | 0256       | 0xAE         | 10101110   | ®      | \&#174;     | \&reg;    | Registered trade mark sign                 |                                    |
| 175        | 0257       | 0xAF         | 10101111   | ¯      | \&#175;     | \&macr;   | Spacing macron - overline                  |                                    |
| 176        | 0260       | 0xB0         | 10110000   | °      | \&#176;     | \&deg;    | Degree sign                                | 温度符号                           |
| 177        | 0261       | 0xB1         | 10110001   | ±      | \&#177;     | \&plusmn; | Plus-or-minus sign                         | 加/减号                            |
| 178        | 0262       | 0xB2         | 10110010   | ²      | \&#178;     | \&sup2;   | Superscript two - squared                  | 上标 2                             |
| 179        | 0263       | 0xB3         | 10110011   | ³      | \&#179;     | \&sup3;   | Superscript three - cubed                  | 上标 3                             |
| 180        | 0264       | 0xB4         | 10110100   | ´      | \&#180;     | \&acute;  | Acute accent - spacing acute               |                                    |
| 181        | 0265       | 0xB5         | 10110101   | µ      | \&#181;     | \&micro;  | Micro sign                                 | 微符号                             |
| 182        | 0266       | 0xB6         | 10110110   | ¶      | \&#182;     | \&para;   | Pilcrow sign - paragraph sign              | 段落符号， pilcrow                 |
| 183        | 0267       | 0xB7         | 10110111   | ·      | \&#183;     | \&middot; | Middle dot - Georgian comma                | 中点                               |
| 184        | 0270       | 0xB8         | 10111000   | ¸      | \&#184;     | \&cedil;  | Spacing cedilla                            |                                    |
| 185        | 0271       | 0xB9         | 10111001   | ¹      | \&#185;     | \&sup1;   | Superscript one                            | 上标 1                             |
| 186        | 0272       | 0xBA         | 10111010   | º      | \&#186;     | \&ordm;   | Masculine ordinal indicator                | 阳性顺序 指示符                    |
| 187        | 0273       | 0xBB         | 10111011   | »      | \&#187;     | \&raquo;  | Right double angle quotes                  | 右角引号                           |
| 188        | 0274       | 0xBC         | 10111100   | ¼      | \&#188;     | \&frac14; | Fraction one quarter                       | 分数四分之一                       |
| 189        | 0275       | 0xBD         | 10111101   | ½      | \&#189;     | \&frac12; | Fraction one half                          | 分数二分之一                       |
| 190        | 0276       | 0xBE         | 10111110   | ¾      | \&#190;     | \&frac34; | Fraction three quarters                    |                                    |
| 191        | 0277       | 0xBF         | 10111111   | ¿      | \&#191;     | \&iquest; | Inverted question mark                     | 反向问号                           |
| 192        | 0300       | 0xC0         | 11000000   | À      | \&#192;     | \&Agrave; | Latin capital letter A with grave          | 带重音符 的大写字母 A              |
| 193        | 0301       | 0xC1         | 11000001   | Á      | \&#193;     | \&Aacute; | Latin capital letter A with acute          | 带尖锐重音 的大写字母 A            |
| 194        | 0302       | 0xC2         | 11000010   | Â      | \&#194;     | \&Acirc;  | Latin capital letter A with circumflex     | 带音调符号 的大写字母 A            |
| 195        | 0303       | 0xC3         | 11000011   | Ã      | \&#195;     | \&Atilde; | Latin capital letter A with tilde          | 带代字号 的大写字母 A              |
| 196        | 0304       | 0xC4         | 11000100   | Ä      | \&#196;     | \&Auml;   | Latin capital letter A with diaeresis      | 带元音变音 (分音符号) 的大写字母 A |
| 197        | 0305       | 0xC5         | 11000101   | Å      | \&#197;     | \&Aring;  | Latin capital letter A with ring above     | 带铃声 的大写字母 A                |
| 198        | 0306       | 0xC6         | 11000110   | Æ      | \&#198;     | \&AElig;  | Latin capital letter AE                    | 大写字母 AE 双重元音               |
| 199        | 0307       | 0xC7         | 11000111   | Ç      | \&#199;     | \&Ccedil; | Latin capital letter C with cedilla        | 带变音符号 的大写字母 C            |
| 200        | 0310       | 0xC8         | 11001000   | È      | \&#200;     | \&Egrave; | Latin capital letter E with grave          | 带重音符 的大写字母 E              |
| 201        | 0311       | 0xC9         | 11001001   | É      | \&#201;     | \&Eacute; | Latin capital letter E with acute          | 带尖锐重音 的大写字母 E            |
| 202        | 0312       | 0xCA         | 11001010   | Ê      | \&#202;     | \&Ecirc;  | LatincapitalletterEwithcircumflex          | 带音调符号 的大写字母 E            |
| 203        | 0313       | 0xCB         | 11001011   | Ë      | \&#203;     | \&Euml;   | Latin capital letter E with diaeresis      | 带元音变音 (分音符号) 的大写字母 E |
| 204        | 0314       | 0xCC         | 11001100   | Ì      | \&#204;     | \&Igrave; | Latin capital letter I with grave          | 带重音符 的大写字母 I              |
| 205        | 0315       | 0xCD         | 11001101   | Í      | \&#205;     | \&Iacute; | Latin capital letter I with acute          | 带尖锐重音 的大写字母 I            |
| 206        | 0316       | 0xCE         | 11001110   | Î      | \&#206;     | \&Icirc;  | Latin capital letter I with circumflex     | 带音调符号 的大写字母 I            |
| 207        | 0317       | 0xCF         | 11001111   | Ï      | \&#207;     | \&Iuml;   | Latin capital letter I with diaeresis      | 带元音变音 (分音符号) 的大写字母 I |
| 208        | 0320       | 0xD0         | 11010000   | Ð      | \&#208;     | \&ETH;    | Latin capital letter ETH                   |                                    |
| 209        | 0321       | 0xD1         | 11010001   | Ñ      | \&#209;     | \&Ntilde; | Latin capital letter N with tilde          | 带代字号 的大写字母 N              |
| 210        | 0322       | 0xD2         | 11010010   | Ò      | \&#210;     | \&Ograve; | Latin capital letter O with grave          | 带重音符 的大写字母 O              |
| 211        | 0323       | 0xD3         | 11010011   | Ó      | \&#211;     | \&Oacute; | Latin capital letter O with acute          | 带尖锐重音 的大写字母 O            |
| 212        | 0324       | 0xD4         | 11010100   | Ô      | \&#212;     | \&Ocirc;  | Latin capital letter O with circumflex     | 带音调符号 的大写字母 O            |
| 213        | 0325       | 0xD5         | 11010101   | Õ      | \&#213;     | \&Otilde; | Latin capital letter O with tilde          | 带代字号 的大写字母 O              |
| 214        | 0326       | 0xD6         | 11010110   | Ö      | \&#214;     | \&Ouml;   | Latin capital letter O with diaeresis      | 带元音变音 (分音符号) 的大写字母 O |
| 215        | 0327       | 0xD7         | 11010111   | ×      | \&#215;     | \&times;  | Multiplication sign                        | 大写字母 OE 连字                   |
| 216        | 0330       | 0xD8         | 11011000   | Ø      | \&#216;     | \&Oslash; | Latin capital letter O with slash          | 带斜杠 的大写字母 O                |
| 217        | 0331       | 0xD9         | 11011001   | Ù      | \&#217;     | \&Ugrave; | Latin capital letter U with grave          | 带重音符 的大写字母 U              |
| 218        | 0332       | 0xDA         | 11011010   | Ú      | \&#218;     | \&Uacute; | Latin capital letter U with acute          | 带尖锐重音 的大写字母 U            |
| 219        | 0333       | 0xDB         | 11011011   | Û      | \&#219;     | \&Ucirc;  | Latin capital letter U with circumflex     | 带音调符号 的大写字母 U            |
| 220        | 0334       | 0xDC         | 11011100   | Ü      | \&#220;     | \&Uuml;   | Latin capital letter U with diaeresis      | 带元音变音 (分音符号) 的大写字母 U |
| 221        | 0335       | 0xDD         | 11011101   | Ý      | \&#221;     | \&Yacute; | Latin capital letter Y with acute          | 带元音变音 (分音符号) 的大写字母 Y |
| 222        | 0336       | 0xDE         | 11011110   | Þ      | \&#222;     | \&THORN;  | Latin capital letter THORN                 |                                    |
| 223        | 0337       | 0xDF         | 11011111   | ß      | \&#223;     | \&szlig;  | Latin small letter sharp s - ess-zed       | 德语高调 小写字母 s                |
| 224        | 0340       | 0xE0         | 11100000   | à      | \&#224;     | \&agrave; | Latin small letter a with grave            | 带重音符 的小写字母 a              |
| 225        | 0341       | 0xE1         | 11100001   | á      | \&#225;     | \&aacute; | Latin small letter a with acute            | 带尖锐重音 的小写字母 a            |
| 226        | 0342       | 0xE2         | 11100010   | â      | \&#226;     | \&acirc;  | Latin small letter a with circumflex       | 带音调符号 的小写字母 a            |
| 227        | 0343       | 0xE3         | 11100011   | ã      | \&#227;     | \&atilde; | Latin small letter a with tilde            | 带代字号 的小写字母 a              |
| 228        | 0344       | 0xE4         | 11100100   | ä      | \&#228;     | \&auml;   | Latin small letter a with diaeresis        | 带元音变音 (分音符号) 的小写字母 a |
| 229        | 0345       | 0xE5         | 11100101   | å      | \&#229;     | \&aring;  | Latin small letter a with ring above       | 带铃声的 小写字母 a                |
| 230        | 0346       | 0xE6         | 11100110   | æ      | \&#230;     | \&aelig;  | Latin small letter ae                      | 小写字母 ae 双重元音               |
| 231        | 0347       | 0xE7         | 11100111   | ç      | \&#231;     | \&ccedil; | Latin small letter c with cedilla          | 带变音符号 的小写字母 c            |
| 232        | 0350       | 0xE8         | 11101000   | è      | \&#232;     | \&egrave; | Latin small letter e with grave            | 带重音符 的小写字母 e              |
| 233        | 0351       | 0xE9         | 11101001   | é      | \&#233;     | \&eacute; | Latin small letter e with acute            | 带尖锐重音 的小写字母 e            |
| 234        | 0352       | 0xEA         | 11101010   | ê      | \&#234;     | \&ecirc;  | Latin small letter e with circumflex       | 带音调符号 的小写字母 e            |
| 235        | 0353       | 0xEB         | 11101011   | ë      | \&#235;     | \&euml;   | Latin small letter e with diaeresis        | 带元音变音 (分音符号) 的小写字母 e |
| 236        | 0354       | 0xEC         | 11101100   | ì      | \&#236;     | \&igrave; | Latin small letter i with grave            | 带重音符 的小写字母 i              |
| 237        | 0355       | 0xED         | 11101101   | í      | \&#237;     | \&iacute; | Latin small letter i with acute            | 带尖锐重音 的小写字母 i            |
| 238        | 0356       | 0xEE         | 11101110   | î      | \&#238;     | \&icirc;  | Latin small letter i with circumflex       | 带音调符号 的小写字母 i            |
| 239        | 0357       | 0xEF         | 11101111   | ï      | \&#239;     | \&iuml;   | Latin small letter i with diaeresis        | 带元音变音 (分音符号) 的小写字母 i |
| 240        | 0360       | 0xF0         | 11110000   | ð      | \&#240;     | \&eth;    | Latin small letter eth                     |                                    |
| 241        | 0361       | 0xF1         | 11110001   | ñ      | \&#241;     | \&ntilde; | Latin small letter n with tilde            | 带代字号 的小写字母 n              |
| 242        | 0362       | 0xF2         | 11110010   | ò      | \&#242;     | \&ograve; | Latin small letter o with grave            | 带重音符 的小写字母 o              |
| 243        | 0363       | 0xF3         | 11110011   | ó      | \&#243;     | \&oacute; | Latin small letter o with acute            | 带尖锐重音 的小写字母 o            |
| 244        | 0364       | 0xF4         | 11110100   | ô      | \&#244;     | \&ocirc;  | Latin small letter o with circumflex       | 带音调符号 的小写字母 o            |
| 245        | 0365       | 0xF5         | 11110101   | õ      | \&#245;     | \&otilde; | Latin small letter o with tilde            | 带代字号 的小写字母 o              |
| 246        | 0366       | 0xF6         | 11110110   | ö      | \&#246;     | \&ouml;   | Latin small letter o with diaeresis        | 带元音变音 (分音符号) 的小写字母 o |
| 247        | 0367       | 0xF7         | 11110111   | ÷      | \&#247;     | \&divide; | Division sign                              | 小写字母 oe 连字                   |
| 248        | 0370       | 0xF8         | 11111000   | ø      | \&#248;     | \&oslash; | Latin small letter o with slash            | 带斜杠 的小写字母 o                |
| 249        | 0371       | 0xF9         | 11111001   | ù      | \&#249;     | \&ugrave; | Latin small letter u with grave            | 带重音符 的小写字母 u              |
| 250        | 0372       | 0xFA         | 11111010   | ú      | \&#250;     | \&uacute; | Latin small letter u with acute            | 带尖锐重音 的小写字母 u            |
| 251        | 0373       | 0xFB         | 11111011   | û      | \&#251;     | \&ucirc;  | Latin small letter u with circumflex       | 带音调符号 的小写字母 u            |
| 252        | 0374       | 0xFC         | 11111100   | ü      | \&#252;     | \&uuml;   | Latin small letter u with diaeresis        | 带元音变音 (分音符号) 的小写字母 u |
| 253        | 0375       | 0xFD         | 11111101   | ý      | \&#253;     | \&yacute; | Latin small letter y with acute            | 带元音变音 (分音符号) 的小写字母 y |
| 254        | 0376       | 0xFE         | 11111110   | þ      | \&#254;     | \&thorn;  | Latin small letter thorn                   |                                    |
| 255        | 0377       | 0xFF         | 11111111   | ÿ      | \&#255;     | \&yuml;   | Latin small letter y with diaeresis        |                                    |
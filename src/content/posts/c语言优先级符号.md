---
title: c语言优先级符号
published: 2024-08-14
description: ''
image: ''
tags: [c]
category: 'c语言'
draft: false 
lang: ''
---




**初级运算符**( )、[ ]、->、.  高于  **单目运算符**  高于  **算数运算符**（先乘除后加减）  高于  **关系运算符**  高于  **逻辑运算符**（不包括！）  高于  **条件运算符**  高于  **赋值运算符**  高于  **逗号运算符。**

**位运算符**的优先级比较分散。

除了赋值运算符、条件运算符、单目运算符三类的平级运算符之间的结合顺序是**从右至左**，其他都是从左至右。

C语言运算符优先级



<table>
  <thead>
    <tr>
      <th>优先级</th>
      <th>运算符</th>
      <th>名称或含义</th>
      <th>使用形式</th>
      <th>结合方向</th>
      <th>说明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">1</td>
      <td>[]</td>
      <td>数组下标</td>
      <td>数组名[常量表达式]</td>
      <td rowspan="4">左到右</td>
      <td>—</td>
    </tr>
    <tr>
      <td>()</td>
      <td>圆括号</td>
      <td>(表达式）/函数名(形参表)</td>
      <td>—</td>
    </tr>
    <tr>
      <td>.</td>
      <td>成员选择（对象）</td>
      <td>对象.成员名</td>
      <td>—</td>
    </tr>
    <tr>
      <td>-></td>
      <td>成员选择（指针）</td>
      <td>对象指针->成员名</td>
      <td>—</td>
    </tr>
    <tr>
      <td rowspan="9">2</td>
      <td>–</td>
      <td>负号运算符</td>
      <td>-表达式</td>
      <td rowspan="9">右到左</td>
      <td rowspan="7">单目运算符</td>
    </tr>
    <tr>
      <td>~</td>
      <td>按位取反运算符</td>
      <td>~表达式</td>
    </tr>
    <tr>
      <td>++</td>
      <td>自增运算符</td>
      <td>++变量名/变量名++</td>
    </tr>
    <tr>
      <td>—</td>
      <td>自减运算符</td>
      <td>–变量名/变量名–</td>
    </tr>
    <tr>
      <td>*</td>
      <td>取值运算符</td>
      <td>*指针变量</td>
    </tr>
    <tr>
      <td>&</td>
      <td>取地址运算符</td>
      <td>&变量名</td>
    </tr>
    <tr>
      <td>!</td>
      <td>逻辑非运算符</td>
      <td>!表达式</td>
    </tr>
    <tr>
      <td>(类型)</td>
      <td>强制类型转换</td>
      <td>(数据类型)表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>sizeof</td>
      <td>长度运算符</td>
      <td>sizeof(表达式)</td>
      <td>—</td>
    </tr>
    <tr>
      <td rowspan="3">3</td>
      <td>/</td>
      <td>除</td>
      <td>表达式/表达式</td>
      <td rowspan="3">左到右</td>
      <td rowspan="3">双目运算符</td>
    </tr>
    <tr>
      <td>*</td>
      <td>乘</td>
      <td>表达式*表达式</td>
    </tr>
    <tr>
      <td>%</td>
      <td>余数（取模）</td>
      <td>整型表达式%整型表达式</td>
    </tr>
    <tr>
      <td rowspan="2">4</td>
      <td>+</td>
      <td>加</td>
      <td>表达式+表达式</td>
      <td rowspan="2">左到右</td>
      <td rowspan="2">双目运算符</td>
    </tr>
    <tr>
      <td>–</td>
      <td>减</td>
      <td>表达式-表达式</td>
    </tr>
    <tr>
      <td rowspan="2">5</td>
      <td><<</td>
      <td>左移</td>
      <td>变量<<表达式</td>
      <td rowspan="2">左到右</td>
      <td rowspan="2">双目运算符</td>
    </tr>
    <tr>
      <td>>></td>
      <td>右移</td>
      <td>变量>>表达式</td>
    </tr>
    <tr>
      <td rowspan="4">6</td>
      <td>></td>
      <td>大于</td>
      <td>表达式>表达式</td>
      <td rowspan="4">左到右</td>
      <td rowspan="4">双目运算符</td>
    </tr>
    <tr>
      <td>>=</td>
      <td>大于等于</td>
      <td>表达式>=表达式</td>
    </tr>
    <tr>
      <td><</td>
      <td>小于</td>
      <td>表达式<表达式</td>
    </tr>
    <tr>
      <td><=</td>
      <td>小于等于</td>
      <td>表达式<=表达式</td>
    </tr>
    <tr>
      <td rowspan="2">7</td>
      <td>==</td>
      <td>等于</td>
      <td>表达式==表达式</td>
      <td rowspan="2">左到右</td>
      <td rowspan="2">双目运算符</td>
    </tr>
    <tr>
      <td>!=</td>
      <td>不等于</td>
      <td>表达式!= 表达式</td>
    </tr>
    <tr>
      <td>8</td>
      <td>&</td>
      <td>按位与</td>
      <td>表达式&表达式</td>
      <td>左到右</td>
      <td>双目运算符</td>
    </tr>
    <tr>
      <td>9</td>
      <td>^</td>
      <td>按位异或</td>
      <td>表达式^表达式</td>
      <td>左到右</td>
      <td>双目运算符</td>
    </tr>
    <tr>
      <td>10</td>
      <td>|</td>
      <td>按位或</td>
      <td>表达式|表达式</td>
      <td>左到右</td>
      <td>双目运算符</td>
    </tr>
    <tr>
      <td>11</td>
      <td>&&</td>
      <td>逻辑与</td>
      <td>表达式&&表达式</td>
      <td>左到右</td>
      <td>双目运算符</td>
    </tr>
    <tr>
      <td>12</td>
      <td>||</td>
      <td>逻辑或</td>
      <td>表达式||表达式</td>
      <td>左到右</td>
      <td>双目运算符</td>
    </tr>
    <tr>
      <td>13</td>
      <td>?:</td>
      <td>条件运算符</td>
      <td>表达式1?表达式2: 表达式3</td>
      <td>右到左</td>
      <td>三目运算符</td>
    </tr>
    <tr>
      <td rowspan="11">14</td>
      <td>=</td>
      <td>赋值运算符</td>
      <td>变量=表达式</td>
      <td rowspan="11">右到左</td>
      <td>—</td>
    </tr>
    <tr>
      <td>/=</td>
      <td>除后赋值</td>
      <td>变量/=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>*=</td>
      <td>乘后赋值</td>
      <td>变量*=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>%=</td>
      <td>取模后赋值</td>
      <td>变量%=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>+=</td>
      <td>加后赋值</td>
      <td>变量+=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>-=</td>
      <td>减后赋值</td>
      <td>变量-=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td><<=</td>
      <td>左移后赋值</td>
      <td>变量<<=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>>>=</td>
      <td>右移后赋值</td>
      <td>变量>>=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>&=</td>
      <td>按位与后赋值</td>
      <td>变量&=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>^=</td>
      <td>按位异或后赋值</td>
      <td>变量^=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>|=</td>
      <td>按位或后赋值</td>
      <td>变量|=表达式</td>
      <td>—</td>
    </tr>
    <tr>
      <td>15</td>
      <td>,</td>
      <td>逗号运算符</td>
      <td>表达式,表达式,…</td>
      <td>左到右</td>
      <td>—</td>
    </tr>
  </tbody>
</table>





说明： 同一优先级的运算符，运算次序由结合方向所决定。

简单记就是：！ > 算术运算符 > 关系运算符 > && > || > 赋值运算符

版权声明：本文内容由互联网用户自发贡献，该文观点仅代表作者本人。本站仅提供信息存储空间服务，不拥有所有权，不承担相关法律责任。如发现本站有涉嫌侵权/违法违规的内容， 请发送邮件至 举报，一经查实，本站将立刻删除。 

发布者：全栈程序员栈长，转载请注明出处：https://javaforall.cn/185808.html原文链接：https://javaforall.cn




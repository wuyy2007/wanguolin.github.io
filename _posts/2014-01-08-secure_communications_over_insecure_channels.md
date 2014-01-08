---
layout: post
title: "在不可信的环境下建立可信连接"
description: ""
category: 技术笔记
tags: [密码学]
---
{% include JB/setup %}


主流密码学的本质是信息的变幻。古典密码学更是由代换和置换（substitution and transposition）[1] 这两种基本技巧所组成。比方最早期据说由凯撒大帝发明的Caesar密码，就是将26个字母分别以其后顺位第三个字母所替换：

`abcd  =>  defg       hello => khooq`

如果26个字母映射为数字，将位移扩展为k，就得到一般的Caesar算法公式：

`加密算法：C = E(p) = (p + k)mod(26)    解密算法： p = D(C) = （C - k）mod(26)`

再上面的公式中，p代表原文，C是密文，k是加密过程中的需要的重要参数，也是由密文还原出原文所需要的重要参数，如果借用现实生活中钥匙的比喻，k即是这个算法中的Key。

对于所有基于代换的派生算法，凡是可以转化为k的一元一次的加密公式的，都存在着一个统一的攻击思路：词频统计。基于大数定理，对于给定的自然语言，或是某个特定的消息集合，其26个字母的出现频率将收敛至某个常数频率。那么基于对密文的词频扫描，就可以推出他们和原文中同等词频的映射关系，进而求解出k。


`某数字公司漏洞修复代码中的漏洞信息数据库就是通过简单异或来加密一个xml的纯文本，可以通过词频统计出高频字符的范围来猜解被异或的数字，由于xml的首字符是<，更可以写出高效的猜解代码`


为了屏蔽词频信息，出现了加密复杂度更高的多表代换算法，以Hill为例，这是1929年由数学家Lester Hill发明的。其加密算法是将m个连续的明文字母替换成m个密文字母。如果把26个字母映射为数字，

$$ a^2 $$

[1]: (/assets/cryptography_and_network_security.pdf) "Cryptography and Network Security - Principles and Practice, Chapter 2.2.2, Substitution Techniques. 《密码编码学与网络信息安全》"







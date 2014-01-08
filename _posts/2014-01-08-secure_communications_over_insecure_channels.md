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

`C = E(p) = (p + k)mod(26)`

[1]: "Cryptography and Network Security, Principles and Practice" (/assets/cryptography_and_network_security.pdf)






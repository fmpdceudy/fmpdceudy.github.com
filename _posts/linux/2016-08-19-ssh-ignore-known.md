---
layout:     post
title:      ssh ignore known_host
categories: linux ssh
---

当登录其他机器时有时需要禁用known_host检查，需要做如下修改

1. 修改配置文件~/.ssh/config, 添加如下两行

        StrictHostKeyChecking no
        UserKnownHostsFile /dev/null

2. 重启ssh服务

当做完这些修改之后, ssh登陆其他机器时将不再检查known_host


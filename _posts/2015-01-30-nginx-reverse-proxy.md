---
layout: post
title: Nginx ��������͸��ؾ���
---

# Nginx ��������͸��ؾ���

#### ʲô���������

�����������һ�����壬�򵥵�˵������һ���û����ҷ��ʲ���ĳ��վ���������ܷ���һ�������������������������������ȥ������Ҫ����ҳ����ȡ�������ҡ�����վ�ĽǶȣ�����ֻ�д����������ķ��ʼ�¼������֪�����û�������Ҳ�������û������ϣ���ȡ���ڴ����治������վ�����Ƿ�ת�� X-REAL-IP����

#### ʲô�Ƿ��������

������������������Ŀ����վ��������һ�ѷ����������û�ֻ֪������������IP������֪������ʵ���ʵ���̨����������������ʵ�����˵�Ŀ����վ�ĸ��ؾ��⣩��ʱ��������������Ŀ����վ��һ��ġ��û�����ֻ�д���������������Ҳ��֪�������ڷ��ʵ���һ��������

#### Nginx �򵥵ķ������

�ڴ����������� nginx.conf �� http ���������ã�

    location / {
        proxy_pass        http://Ŀ�����IP:�˿�;
        proxy_set_header  X-Real-IP  $remote_addr; # ת���û�����ʵIP
    }

�����ǵ�̨���������Ҫ������̨������Ҫ�õ� upstream ģ�飨���ؾ��⣩��

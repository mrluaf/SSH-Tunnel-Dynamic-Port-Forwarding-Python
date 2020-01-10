# SSH Tunnel Dynamic Port Forwarding Python

![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)

# New Features!
  - Hoạt động trên tất cả các hệ điều hành: Window, UNIX
  - Chỉ mới thử nghiệm trên Python 3.x

## Giới thiệu

Một thư viện sử dụng để enable kết nối SSH về Socks5 Proxy.
Giống như cách sử dụng OpenSSH.
>ssh -D 1080 -N username@host

## Ví dụ
```python
def test(host, username, password, port):
  controlssh = SSHProxyControler(host, username, password, port)
  sshstatus, host, port = controlssh.start()
  print(sshstatus, host, port)
  if sshstatus:

    time.sleep(30) #Make some request right here

    controlssh.stop()
    print('SSH is Stoped')
  else:
    print('Can not connect to SSH')

test('14.177.235.133', 'admin', 'admin', 1082)

```

## Installation
```
pip3 install asyncssh
```
* [asyncssh] - Full support for SSHv2, SFTP, and SCP client and server functions

<link rel="stylesheet" type="text/css" href="//code.ionicframework.com/ionicons/2.0.1/css/ionicons.min.css" />
Made with <i class="icon ion-heart"></i> in Switzerland

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen.)

    
   [asyncssh]: <https://pypi.org/project/asyncssh/>


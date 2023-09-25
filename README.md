# Preface

The Python Command-line Reimplementaion of Google Authenticator:

![](https://skywind3000.github.io/images/p/misc/2023/googauth.png)


## Get started

Edit a configuration in ini format:

```ini
[test.com]
user=username1
secret=GEZDGNBVGY3TQYLG
domain=https://test1.com

[huobi.com]
user=username2
secret=HEZDGNBVGY3TQYLF
domain=https://huobi.com
```

The secret field is a base32-encoded secret code provided by your site.

Get the authenticator code by:

```bash
$ python3 googauth.py -l test.ini
```

It will display the codes like:

```text
+-----------+-------------------+--------+-----------+
| User      | Domain            | Code   | Life Time |
+-----------+-------------------+--------+-----------+
| username2 | https://huobi.com | 994604 |   27 (s)  |
+-----------+-------------------+--------+-----------+
| username1 | https://test1.com | 683903 |   27 (s)  |
+-----------+-------------------+--------+-----------+
```

a bash alias could be created for convenience:

```bash
$ alias googauth='python3 /path/to/googauth.py -l ~/.config/googauth.ini'
```

Done.


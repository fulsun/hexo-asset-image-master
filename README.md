# hexo-asset-image
官方`hexo-asset-image`插件，在同时使用`hexo-abbrlink`时，会导致图片路径错误。

本插件是基于官方插件1.0.0的修改，为了解决域名是xxx.io的情况下，图片路径会从原本/xxx.jpg变成 /.io/xxx.jpg

# Usege

```shell
npm install https://github.com/fulsun/hexo-asset-image-master.git --save
```

# Example

> 同时使用hexo-abbrlink

```yaml
root: /
permalink: posts/:abbrlink.html
abbrlink:
  alg: crc32  # 算法：crc16(default) and crc32
  rep: hex    # 进制：dec(default) and hex
```

> 目录结构

```shell
test
├── logo.jpg
└── rules.jpg
test.md
```

> 用法

Make sure `post_asset_folder: true` in your `_config.yml`.

```sh
![logo](test/logo.jpg)
```


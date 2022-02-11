# hexo-asset-image
官方`hexo-asset-image`插件，在同时使用`hexo-abbrlink`时，会导致图片路径错误。

本插件是基于官方插件1.0.0的修改，为了解决域名是xxx.io的情况下，图片路径会从原本/xxx.jpg变成 /.io/xxx.jpg

# Usege

1. 配置

   `_config.yml`配置文件中设置`post_asset_folder: true` 

2. 添加依赖

   ```sh
   npm install https://github.com/fulsun/hexo-asset-image-master.git --save
   npm install hexo-abbrlink --save
   ```

3. 指定文章链接

   ```sh
   root: /
   permalink: posts/:abbrlink.html
   pretty_urls:
     trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
     trailing_html: false # Set to false to remove trailing '.html' from permalinks
   
   abbrlink:
     alg: crc32  # 算法：crc16(default) and crc32
     rep: hex    # 进制：dec(default) and hex
   ```

   

# Example

- 目录结构

  ```sh
  test
  ├── logo.jpg
  └── rules.jpg
  test.md
  ```

- markdown中的用法,在typora中也能查看图片

  ```sh
  ![logo](test/logo.jpg)
  ```

  


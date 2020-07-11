* npm install hexo 
* hexo init wangjstu.github.io		//初始化blog
* cd wangjstu.github.io
* npm install
* npm install hexo-deployer-git
* git init
* git remote add origin git@github.com:wangjstu/wangjstu.github.io.git
* git clone https://github.com/cofess/hexo-theme-pure.git themes/pure
* 配置`_config.yml`



* git clone https://github.com/cofess/hexo-theme-pure.git themes/pure
* cd themes/pure
* git pull
* 安装插件
  * npm install hexo-wordcount --save
  * npm install hexo-generator-json-content --save
  * npm install hexo-generator-feed --save
  * npm install hexo-generator-sitemap --save
  * npm install hexo-generator-sitemap --save
  * npm install hexo-generator-baidu-sitemap --save
* npm install hexo-neat --save
```SHELL
You can configure this plugin in _config.yml.

# hexo-neat
neat_enable: true
neat_html:
  enable: true
  exclude:  
neat_css:
  enable: true
  exclude:
    - '*.min.css'
neat_js:
  enable: true
  mangle: true
  output:
  compress:
  exclude:
    - '*.min.js'
```




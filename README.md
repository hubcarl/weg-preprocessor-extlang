weg-preprocessor-extlang
===========================

An fis preproccessor plugin for parse swig custom tags.

支持使用Swig script, style 插件的JavaScript的语言扩展

```tpl
{% script %}
    require('./a.js');
    __inline('./b.js');
    var a = __uri('./c.js');
    //blabla
{% endscript %}

{% style %}
@import url(./a.css?__inline);
{% endstyle %}
```

使用
====

```bash
// install
npm install -g weg-preprocessor-extlang
```

```bash
// config
vi <project>/fis-conf.js

fis.match('/client/views/(**).tpl', {
    useMap:true,
    url: '/$1',
    preprocessor: fis.plugin('extlang')
});
```


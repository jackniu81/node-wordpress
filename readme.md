# node-wordpress

A node.js JavaScript client for working with WordPress.


Requires WordPress 3.4 or newer (uses the [WordPress XML-RPC API](http://codex.wordpress.org/XML-RPC_WordPress_API)).

## Install
```
 npm install wordpress
```
 
## Usage
Include the wordpress package
```js
var wordpress = require('wordpress');
var wpClient = wordpress.createClient({
    "url": 'http://yourwordpressURL', 
    "username": 'user', 
    "password": 'pwd' 
});
```

### Demo of post
```js
wpClient.newPost({
        title: 'Your title',
        status: 'publish', //'publish, draft...',
        content: '<strong>This is the content</strong>',
        termNames: {'category': ['cate1', 'cate2'], 'post_tag':['tag1', 'tag2']}
    },
    function() { 
        console.log(arguments);
    }
});
```



## License

MIT license

### query-string
---
https://github.com/sindresorhus/query-string

```sh
npm install query-string
```

```js
const queryString = require('query-string');
console.log(location.search);

const parsed = queryString.parse(location.search);
console.log(parsed);

console.log(location.hash);

const parsedHash = queryString.parse(location.hash);
console.log(parsedHash);

parsed.foo = 'unicorn';
parsed.ilike = 'pizza';

const stringified = queryString.stringify(parsed);
location.search = stringified;
console.log(location.search);

queryString.parse('foo[]=1&foo[]=2&foo[]=3', {arrayFormat: 'bracket'});

queryString.parse('foo[0]=1&foo[1]=2&foo[3]=3', {arrayFormat: 'index'});

queryString.parse('foo=1&foo=2&foo=3');

queryString.stringfy({foo: [1,2,3]}, {arrayFormat: 'bracket'});
qyeryString.stringify({foo: [1,2,3]}, {arrayFormat: 'index'});
queryString.stringify({foo: [1,2,3]});

const order = ['c', 'a', 'b'];
qyeryString.stringfy({a: 1, b: 2, c: 3}, {
  sort: (m, n) => order.indexOf(m) >= order.indexOf(n)
});
queryString.stringify({ b: 1, c: 2, a: 3}, {sort: false});

queryString.parseUrl('https://foo.bar?foo=bar');

queryString.stringfiry({
  foo: 'bar',
  nested: JSON.stringify({
    unicorn: 'cake'
  })
});

queryString.parse('likes=cake&name=bob&likes=icecream');
queryString.stringify({color: ['taupe', 'chartreuse'], id: '515'});

queryString.stringify({foo: false});
queryString.stringify({foo: null});
queryString.stringify({foo: undefined});
```

```
```


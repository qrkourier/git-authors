# git-authors

Print a list of dictionaries describing all the authors that have contributed to a git project in descending order, based on the number of commits.

The Git working copy must be addressable as a filesystem path e.g. /home/alice/Sites/example-project/.

## Usage

NodeJS Command-line Example:
```bash
REPO=~/Sites/example-project node ./example.js
```

Javascript Example:

```js
gitAuthors(repoPath, [revision], callback);
```

```js
var gitAuthors = require('git-authors');
var path = require('path');
var repoPath = path.resolve(process.env.REPO || (__dirname + '/.git'));

gitAuthors(repoPath, function(err, list) {
  if (err) { throw err; }

  console.log(list);
});
```

Sample output:

```js
[{
    "commits": "83",
    "name": "James Hall",
    "email": "james@example.com"
}, {
    "commits": "4",
    "name": "Matt Summers",
    "email": "matt@example.com"
}, {
    "commits": "2",
    "name": "Julian Meyer",
    "email": "julian@example.com"
}, {
    "commits": "2",
    "name": "Max Thunder",
    "email": "max@example.com"
}, {
    "commits": "2",
    "name": "John",
    "email": "john@example.com"
}, {
    "commits": "1",
    "name": "Daniel Doe",
    "email": "dan@example.com"
}, {
    "commits": "1",
    "name": "Duncan",
    "email": "duncan@example.com"
}, {
    "commits": "1",
    "name": "Hugh Doe",
    "email": "hugh@example.com"
}, {
    "commits": "1",
    "name": "Mark Doe",
    "email": "mark@example.com"
}, {
    "commits": "1",
    "name": "Maximilian Doe",
    "email": "mx.doe@example.com"
}, {
    "commits": "1",
    "name": "Mikeal Doe",
    "email": "mikeal@example.com"
}, {
    "commits": "1",
    "name": "Max Doe",
    "email": "max.doe@example.com"
}]
```

## Install
```
npm install
```


## Tests
```
npm test
```

## License

MIT

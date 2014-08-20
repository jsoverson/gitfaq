# GIT FAQ

This is the source for the website [gitfaq.org](http://gitfaq.org)

## Why?

Stack Overflow is great but quality varies and it takes parsing to understand what is actually an acceptable answer to
the actual question an individual has.

Man pages are great if you know what you are looking for, but they are not beginner friendly.

The goal here is to get concise, linkable answers to googlable search terms related to git.

## Contributing

1. Fork the repository
2. Make your changes
3. Submit a pull request

### Adding a FAQ

Add FAQ entries, individually, to the `contents/articles/` directory. The filename is the URL so make sure it is terse
yet still includes relevant search terms.

Example file : `how-do-i-commit-a-file.md`

    ---
    title: How do I commit a file?
    template: article.jade
    ---
    ```
    git add file.js # stage the file
    git commit      # commit the file
    ```
 
The front matter contains the displayed title and the template used. The template should always be `article.jade`.

The answer to a question should be as terse as possible, deferring to other FAQs if necessary for clarification.
Editorializing should be limited, notable exceptions are to provide reasoning behind common practice if that
is a large part of why a certain FAQ exists to begin with.

## Building

This is built with wintersmith, install via npm:

```
$ npm install -g wintersmith
```

Preview changes with `wintersmith preview`

```
$ wintersmith preview
```

## License

[MIT](http://opensource.org/licenses/MIT)

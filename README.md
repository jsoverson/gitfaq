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

Add FAQ entries, individually, to the `contents/posts/` directory. The filename is the URL so make sure it is terse
yet still includes relevant search terms.

Example file : `how-do-i-commit-a-file.md`

    ---
    author: "Jarrod Overson"
    date: 2022-7-14
    linktitle: How do I add only a portion of a file?
    title: How do I add only a portion of a file?
    ---

    ```sh
    $ git add --patch <file>
    ```

The answer to a question should be as terse as possible, deferring to other FAQs if necessary for clarification.
Editorializing should be limited, notable exceptions are to provide reasoning behind common practice if that
is a large part of why a certain FAQ exists to begin with.

## Building locally

This site uses the Hugo static site generator. To view the site with local changes, use `hugo server`:

```sh
$ hugo server
```

Your site will be available at [http://127.0.0.1:1313](http://127.0.0.1:1313) by default.

## License

[Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0.html)

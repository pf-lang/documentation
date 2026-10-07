## The purpose and audience of this book

This is the official documentation for the core Pipefish language, its standard libraries, and the tooling that comes with it. It is primarily a work of reference, but it has been written so that it can be used to learn the language by people already familiar with such terms of art as "variable" and "integer".

## The purpose and state of Pipefish

The primary use-case of Pipefish is to be used in production to write and deploy CRUD apps and middleware. Considerations of security, concurrency, performance, tooling, and the need for guarantees of the maintenance of the project mean that it isn't yet usable for its primary use-case unless you want to end your tech career with a real bang.

In the [*Roadmap*](****) page of the companion book [*Pipefish in theory and practice*](****), I explain how we will achieve and maintain production-readiness, and how the wider tech community might contribute to that goal. Until then, Pipefish is a general-purpose language which can be used to meet a number of needs: on your desktop as as an all-purpose scripting and glue language; embedded in Golang applications for situations where its greater dynamism and its leaning towards DSLs make it attractive; as a scripting language for the web; in its web framework for data presentation and educational purposes. Early adopters will doubtless find bugs and rough edges, and would do much for the project by pointing them out.

## Sandboxes

Here is your first Pipefish script.

```pf-ide
cmd

greet(name string) :
  post("Hello " + name + "!"

(n int)! :
  n == 0 :
    1
  n > 0 :
    n * (n-1)!
  else :
    error "can't take the factorial of a negative number"
```

If you try this out in the tui above, you will find that `greet "world"` and `5!` do what you would expect, as will expressions using common built-in functions such as `2 + 2`, or `len "aardvark"`.

## Installing Pipefish

Since this book will be full of sandboxes, there is no need to start your exploration of Pipefish by downloading anything. It can in fact be used entirely in its web editor, as explained [here](****). But if you want to use Pipefish to develop apps, you will probably at least from time to time want the sort of environment supplied by VSCode, and by actually having an operating system, to name just two advantages of working on the desktop.

Instructions for how to install Pipefish locally and use it with VS code can be found on [this page](****) of the book.

## Related documents

* [*Pipefish in theory and practice*](****) explains the project for people who are interested in the field of language development.
* [*Language development in Pipefish*](****) teaches some basic language development concepts using Pipefish as runnable pseudocode to illustrate the algorithms: and in the process, to illustrate the use of Pipefish as a teaching language.
* [*Hamsters and fire*](****) is a Pipefish-powered 2D puzzle game running in your browser, with the source code, and an explanation of how this fits into the web framework (and with fire, and adorable little cricetines).

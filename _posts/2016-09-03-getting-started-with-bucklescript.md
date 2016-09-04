---
layout: post
title:  "Bucklescript getting started"
date:   2016-09-03 08:26:37 -0400
categories: bucklescript javascript
---

Interested in [Bucklescript](https://github.com/bloomberg/bucklescript)? You should be. It's OCaml that compiles to JavaScript. But unlike most compile-to-JS langauges, it's really, really good. Fast. Produces small, legible JavaScript. And it's got some of the best type inference in the business.

Here's how I got up and running on my Mac.

## Install OCaml and friends

First, [install OCaml](https://ocaml.org/docs/install.html). On Mac, this is done like so:

    brew install ocaml
    brew install opam
    opam install utop

Opam is the package manager (e.g. like NPM, gems, nuget) for OCaml. Utop is a really, really nice REPL.

## Setup VS Code:

[https://github.com/hackwaly/vscode-ocaml](https://github.com/hackwaly/vscode-ocaml)

## Set up BuckleScript

    mkdir avl
    cd avl
    npm init
    npm install --save bs-platform

Edit `package.json` and make scripts look like this:

    "scripts" : {
        "build" : "bsc -c avl.ml"
    }

## Test that it all works

Create `hi.ml` and make it look like this:

```ocaml
let () =
  print_endline "hello world"
```

Run

    npm run build
    node hi.js

You should see "hello world" get printed.

Noice!

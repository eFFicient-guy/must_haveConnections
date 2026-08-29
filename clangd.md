`frontend and backend seperation` - 
in modern compiler design, toolchains are split into two distinct roles:

`frontend(editor analysis)` - parses code, checks syntax, builds an abstract syntax tree(AST), and catches errors while you type. 
`clangd` handles this inside your editor. 

`backend(code generation)` - takes the valid source code, optimizes
machine code, and liks the final executable binary.g++ handles this.

`script :`
    {
        clang.arguments:[
            "--query-driver=/usr/bin/g++"
        ]
    }
`what it does ?` -
* is allows clangd to execute your installed compiler in the background
* g++ then tells the location of C++ standard library to clangd
`end result` : clangd uses g++'s location map to parse your code cleanly.

`key advantages` - 
* clangd has ultra fast auto-complete, precise inline error diagnostics, and ast-aware renaming in your editor 
* no vendor lock-in - you are not enforced to compile with clang++ just enjoy modern editor intelligence, so you can esssentially use g++ with clangd to get best of both worlds.
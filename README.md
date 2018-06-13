# Lispy

A lisp inspired language implemented in C.

```lisp
(load "prelude.lispy")

(map print
    (list
        "Hello, World!"                  ;; => "Hello, World!"
        (+ 1 2)                          ;; => 3
        (first { 1 2 3 4 5 })            ;; => 1
        (rest { 1 2 3 4 5 })             ;; => { 2 3 4 5 }
        (sum { 1 2 3 4 5 })              ;; => 15
        (reverse { 1 2 3 4 5 })          ;; => { 5 4 3 2 1 }
        (map (constant 1) { 1 2 3 4 5 }) ;; => { 1 1 1 1 1 }
        (filter identity { 0 1 0 2 0 })  ;; => { 1 2 }
        (zip { 1 2 3 } { "a" "b" "c"})   ;; => {{1 "a"} {2 "b"} {3 "c"}}
    ))
```

Outputs...

```sh
$ ./lispy test.lispy
"Hello, World!"
3
1
{2 3 4 5}
15
{5 4 3 2 1}
{1 1 1 1 1}
{1 2}
{{1 "a"} {2 "b"} {3 "c"}}
```

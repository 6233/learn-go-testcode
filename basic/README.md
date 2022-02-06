# learn-go-testcode
learn go testcode

---


## go test

```
$ go test

--- FAIL: TestS1 (0.00s)
    testMe_test.go:7: s1("123456789") != 9
--- FAIL: TestF2 (0.00s)
    testMe_test.go:43: f1(1) != 1
    testMe_test.go:46: f1(2) != 1
    testMe_test.go:49: f1(10) != 55
FAIL
exit status 1
FAIL	github.com/6233/learn-go-testcode/basic	0.051s

```
----
### OPTION


### `-v`

```
$ go test -v

=== RUN   TestS1
    testMe_test.go:7: s1("123456789") != 9
--- FAIL: TestS1 (0.00s)
=== RUN   TestS2
--- PASS: TestS2 (0.00s)
=== RUN   TestF1
--- PASS: TestF1 (0.00s)
=== RUN   TestF2
    testMe_test.go:43: f1(1) != 1
    testMe_test.go:46: f1(2) != 1
    testMe_test.go:49: f1(10) != 55
--- FAIL: TestF2 (0.00s)
FAIL
exit status 1
FAIL	github.com/6233/learn-go-testcode/basic	0.050s
```

`-count=$n`
```
$ go test -count=2

--- FAIL: TestS1 (0.00s)
    testMe_test.go:7: s1("123456789") != 9
--- FAIL: TestF2 (0.00s)
    testMe_test.go:43: f1(1) != 1
    testMe_test.go:46: f1(2) != 1
    testMe_test.go:49: f1(10) != 55
--- FAIL: TestS1 (0.00s)
    testMe_test.go:7: s1("123456789") != 9
--- FAIL: TestF2 (0.00s)
    testMe_test.go:43: f1(1) != 1
    testMe_test.go:46: f1(2) != 1
    testMe_test.go:49: f1(10) != 55
FAIL
exit status 1
FAIL	github.com/6233/learn-go-testcode/basic	0.042s

```

`-cover`

```
$ go test -cover
--- FAIL: TestS1 (0.00s)
    testMe_test.go:7: s1("123456789") != 9
--- FAIL: TestF2 (0.00s)
    testMe_test.go:43: f1(1) != 1
    testMe_test.go:46: f1(2) != 1
    testMe_test.go:49: f1(10) != 55
FAIL
coverage: 94.7% of statements
exit status 1
FAIL	github.com/6233/learn-go-testcode/basic	0.044s

```


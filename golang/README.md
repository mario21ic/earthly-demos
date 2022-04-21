List:
```
earthly ls
```

Linters:
```
earthly +lint
earthly +staticcheck
```

Cache deps:
```
earthly +deps
```

Build:
```
earthly +build --version=1.0
```

Copy vs From:
```
earthly +with-build
earthly +with-copy
```

Docker image:
```
earthly +docker
earthly +docker --tag="nuevo"
earthly --push +docker
```

Build all:
```
earthly +all
```

Running Docker:
```
earthly -P +hello
earthly -P +hello
earthly -P --no-cache +hello
```

Multiplatform:
```
earthly --platform=linux/amd64 +build --version=1.2
file build/go-example
earthly --platform=linux/arm64 +build --version=1.3
file build/go-example

earthly --platform=linux/arm64 +docker
earthly --platform=linux/amd64 +docker
```

Getting example from internet:
```
earthly --artifact github.com/earthly/earthly/examples/tutorial/go:main+part3/part3 ./part3
```

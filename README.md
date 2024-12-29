# guestbook

```
.
├── Dockerfile
├── Makefile
├── README.md
├── bb.edn
├── build.clj
├── deps.edn
├── env
│   ├── dev
│   │   ├── clj
│   │   │   ├── kit
│   │   │   │   └── guestbook
│   │   │   │       ├── dev_middleware.clj
│   │   │   │       └── env.clj
│   │   │   └── user.clj
│   │   └── resources
│   │       └── logback.xml
│   ├── prod
│   │   ├── clj
│   │   │   └── kit
│   │   │       └── guestbook
│   │   │           └── env.clj
│   │   └── resources
│   │       └── logback.xml
│   └── test
│       └── resources
│           └── logback.xml
├── kit.edn
├── kit.git-config.edn
├── resources
│   └── system.edn
├── src
│   └── clj
│       └── kit
│           └── guestbook
│               ├── config.clj
│               ├── core.clj
│               └── web
│                   ├── controllers
│                   │   └── health.clj
│                   ├── handler.clj
│                   ├── middleware
│                   │   ├── core.clj
│                   │   ├── exception.clj
│                   │   └── formats.clj
│                   └── routes
│                       ├── api.clj
│                       └── utils.clj
└── test
    └── clj
        └── kit
            └── guestbook
                ├── core_test.clj
                └── test_utils.clj

```

Start a [REPL](#repls) in your editor or terminal of choice.

Start the server with:

```clojure
(go)
```

The default API is available under http://localhost:3000/api

System configuration is available under `resources/system.edn`.

To reload changes:

```clojure
(reset)
```

## REPLs

### Cursive

Configure a [REPL following the Cursive documentation](https://cursive-ide.com/userguide/repl.html). Using the default "Run with IntelliJ project classpath" option will let you select an alias from the ["Clojure deps" aliases selection](https://cursive-ide.com/userguide/deps.html#refreshing-deps-dependencies).

### CIDER

Use the `cider` alias for CIDER nREPL support (run `clj -M:dev:cider`). See the [CIDER docs](https://docs.cider.mx/cider/basics/up_and_running.html) for more help.

Note that this alias runs nREPL during development. To run nREPL in production (typically when the system starts), use the kit-nrepl library through the +nrepl profile as described in [the documentation](https://kit-clj.github.io/docs/profiles.html#profiles).

### Command Line

Run `clj -M:dev:nrepl` or `make repl`.

Note that, just like with [CIDER](#cider), this alias runs nREPL during development. To run nREPL in production (typically when the system starts), use the kit-nrepl library through the +nrepl profile as described in [the documentation](https://kit-clj.github.io/docs/profiles.html#profiles).

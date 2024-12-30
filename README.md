# guestbook

This was a quick project to check out web dev in Clojure, based on this
tutorial [here](https://kit-clj.github.io/docs/guestbook.html). 

TODO: 
- [ ] Deploy this 
- [ ] Add the ability to edit the message
- [ ] Fix the styling to match my website
--------
Start a REPL in your editor or terminal of choice.

Start the server with:

```clojure
(go)
```

The default API is found at localhost:3000/api
System configuration is found under `resources/system.edn`

Reload changes:

```clojure
(reset)
```
-------
Here's the directory structure: 

```
.
├── Dockerfile
├── Makefile
├── README.md
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
├── guestbook_dev.db
├── kit.edn
├── log
│   └── kit.guestbook.log
├── resources
│   ├── html
│   │   ├── error.html
│   │   └── home.html
│   ├── migrations
│   │   ├── 20220104235847-add-guestbook-table.down.sql
│   │   └── 20220104235847-add-guestbook-table.up.sql
│   ├── public
│   │   ├── css
│   │   │   └── screen.css
│   │   └── img
│   │       └── kit.png
│   ├── sql
│   │   └── queries.sql
│   └── system.edn
├── src
│   └── clj
│       └── kit
│           └── guestbook
│               ├── config.clj
│               ├── core.clj
│               └── web
│                   ├── controllers
│                   │   ├── guestbook.clj
│                   │   └── health.clj
│                   ├── handler.clj
│                   ├── middleware
│                   │   ├── core.clj
│                   │   ├── exception.clj
│                   │   └── formats.clj
│                   ├── pages
│                   │   └── layout.clj
│                   └── routes
│                       ├── api.clj
│                       ├── pages.clj
│                       └── utils.clj
└── test
    └── clj
        └── kit
            └── guestbook
                └── test_utils.clj

```




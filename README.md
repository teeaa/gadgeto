# Gadgeto!

This is a fork of [loopfz/gadgeto](https://github.com/loopfz/gadgeto) which contain non-merged pull requests on this repository as well as enhancements.

I would like to thank the original author for his amazing library. Tonic is really a game changer for me to write HTTP servers in Golang.

List of changed compared to the original repository (you can also use `git log` to list changes, merged PR from the original repository contains a link to them):

- Allow to retrieve bindHook errors: the original error returned by the bind hooks are now accessible.
- Allows the SetRenderHook to override the mediaType
- fix: make sure a validator exists to avoid panic
- Add support for more content-type
- Dependencies bump
- Allow configuring the bind/render hooks and media type per route

## README:

Author:     Thomas Schaffer
Language:   Golang
License:    MIT

Gadgeto! is a collection of tools that aim to facilitate the development of
REST APIs in Go.
These tools are based on and enrich popular open-source solutions, to provide
higher-level functionalities.

Components:
    - tonic: Based on the REST framework Gin (https://github.com/gin-gonic/gin),
                tonic lets you write simpler handler functions, and handles
                repetitive tasks for you (parameter binding, error handling).

    - zesty: Based on Gorp (https://github.com/go-gorp/gorp), zesty abstracts
                DB specifics for easy (nested) transaction management.

    - iffy: An HTTP testing library for functional/unit tests,
                iffy does all the hard work (http, marshaling, templating...) and
                lets you describe http calls as one-liners, chaining them in complex scenarios.

    - amock: An HTTP mocking library. amock lets you easily write mock objects to inject
                into http clients.
                It does not require any go-generate tricks, and lets you inject mocks
                into existing libraries that may not be properly abstracted through interfaces.

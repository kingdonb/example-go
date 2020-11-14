# Go Quick Start Guide

This guide will walk you through deploying a Go application on [Hephy Workflow][].

## Usage

```console
$ git clone https://github.com/teamhephy/example-go.git
$ cd example-go
$ deis config:set https://github.com/heroku/heroku-buildpack-go#v140
$ deis create
Creating Application... done, created allied-question
Git remote deis added for app allied-question
$ git push deis master
Counting objects: 89, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (67/67), done.
Writing objects: 100% (89/89), 19.23 KiB | 0 bytes/s, done.
Total 89 (delta 37), reused 46 (delta 17)
Starting build... but first, coffee!
-----> Go app detected
-----> Checking Godeps/Godeps.json file.
-----> Installing go1.7... done
-----> Running: go install -v -tags heroku .
       github.com/teamhephy/example-go
-----> Discovering process types
       Procfile declares types -> web
-----> Compiled slug size is 1.9M
Build complete.
Launching App...
Done, allied-question:v2 deployed to Workflow

Use 'deis open' to view this application in your browser

To learn more, use 'deis help' or visit https://deis.com/

To ssh://git@deis-builder.deis.rocks:2222/allied-question.git
 * [new branch]      master -> master
$ curl http://allied-question.deis.rocks
Powered by Hephy
Release v2 on allied-question-v2-web-wudcx
```

## Additional Resources

* [GitHub Project](https://github.com/teamhephy/workflow)
* [Documentation](https://docs.teamhephy.com/)
* [Blog](https://blog.teamhephy.info/)

[Hephy Workflow]: https://github.com/teamhephy/workflow#readme

# messagesrecovery-app

Build runner for **Messages Recovery** (`com.messagesrecovery.app`), an Android app that keeps the messages that reach your notifications, so a message deleted by its sender can still be read.

This repository holds a workflow only. A build run checks out the private app repository with a read-only deploy key, analyses and tests it, builds the signed release APKs and the Play bundle, drives the app on an Android emulator, and uploads everything it made as **one sealed file** (AES-256, key held by the owner). No source, build or log leaves the runner readable.

```sh
gh workflow run build.yml -R Mulhimfy/messagesrecovery-app -f ref=main -f smoke=true
```

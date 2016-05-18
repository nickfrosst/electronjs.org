---
version: v1.1.0
category: API
title: 'Environment Variables'
redirect_from:
    - /docs/v0.24.0/api/environment-variables/
    - /docs/v0.25.0/api/environment-variables/
    - /docs/v0.26.0/api/environment-variables/
    - /docs/v0.27.0/api/environment-variables/
    - /docs/v0.28.0/api/environment-variables/
    - /docs/v0.29.0/api/environment-variables/
    - /docs/v0.30.0/api/environment-variables/
    - /docs/v0.31.0/api/environment-variables/
    - /docs/v0.32.0/api/environment-variables/
    - /docs/v0.33.0/api/environment-variables/
    - /docs/v0.34.0/api/environment-variables/
    - /docs/v0.35.0/api/environment-variables/
    - /docs/v0.36.0/api/environment-variables/
    - /docs/v0.36.3/api/environment-variables/
    - /docs/v0.36.4/api/environment-variables/
    - /docs/v0.36.5/api/environment-variables/
    - /docs/v0.36.6/api/environment-variables/
    - /docs/v0.36.7/api/environment-variables/
    - /docs/v0.36.8/api/environment-variables/
    - /docs/v0.36.9/api/environment-variables/
    - /docs/v0.36.10/api/environment-variables/
    - /docs/v0.36.11/api/environment-variables/
    - /docs/v0.37.0/api/environment-variables/
    - /docs/v0.37.1/api/environment-variables/
    - /docs/v0.37.2/api/environment-variables/
    - /docs/v0.37.3/api/environment-variables/
    - /docs/v0.37.4/api/environment-variables/
    - /docs/v0.37.5/api/environment-variables/
    - /docs/v0.37.6/api/environment-variables/
    - /docs/v0.37.7/api/environment-variables/
    - /docs/v0.37.8/api/environment-variables/
    - /docs/v1.0.0/api/environment-variables/
    - /docs/v1.0.1/api/environment-variables/
    - /docs/v1.1.0/api/environment-variables/
    - /docs/latest/api/environment-variables/
source_url: 'https://github.com/electron/electron/blob/master/docs/api/environment-variables.md'
excerpt: "Control application configuration and behavior without changing code."
---

# Environment variables

> Control application configuration and behavior without changing code.

Some behaviors of Electron are controlled by environment variables, because they
are initialized earlier than command line and the app's code.

Examples on POSIX shells:

```bash
$ export ELECTRON_ENABLE_LOGGING=true
$ electron
```

on Windows console:

```powershell
> set ELECTRON_ENABLE_LOGGING=true
> electron
```

## `ELECTRON_RUN_AS_NODE`

Starts the process as a normal Node.js process.

## `ELECTRON_ENABLE_LOGGING`

Prints Chrome's internal logging to console.

## `ELECTRON_LOG_ASAR_READS`

When Electron reads from an ASAR file, log the read offset and file path to
the system `tmpdir`. The resulting file can be provided to the ASAR module
to optimize file ordering.

## `ELECTRON_ENABLE_STACK_DUMPING`

When Electron crashed, prints the stack trace to console.

This environment variable will not work if `crashReporter` is started.

## `ELECTRON_DEFAULT_ERROR_MODE` _Windows_

Shows Windows's crash dialog when Electron crashed.

This environment variable will not work if `crashReporter` is started.

## `ELECTRON_NO_ATTACH_CONSOLE` _Windows_

Don't attach to current console session.

## `ELECTRON_FORCE_WINDOW_MENU_BAR` _Linux_

Don't use global menu bar on Linux.
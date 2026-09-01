# Overview

[简体中文](overview.zh-CN.md) | [Docs Index](README.md)

## Purpose

SOCKS protocol message, authentication, and command codecs for Gnalloy pipelines.

This module sits above transports and below application handlers. It translates bytes or Gnalloy messages into protocol objects, and translates outbound protocol objects back to bytes. It does not open sockets or own EventLoops.

## Repository Identity

- Module path: `gnalloy.org/codec-socks`
- GitHub repository: `github.com/gnalloy/codec-socks`
- Default branch: `dev`
- License: Apache-2.0

## Package Map
- `gnalloy.org/codec-socks` (`socks`)

## Direct Gnalloy Dependencies

- `gnalloy.org/gnalloy`

## Direct Dependents in the Current Repository Set

- No repository in the current local Gnalloy set directly depends on this module.

## Architecture Position

Gnalloy keeps the core small and dependency-light. This repository is a replaceable module around one responsibility, connected through explicit Go packages instead of runtime discovery.

## Compatibility

The public import path is `gnalloy.org/codec-socks`. Until the first stable tag is published, use `@dev` or an explicit pseudo-version selected by your dependency policy.

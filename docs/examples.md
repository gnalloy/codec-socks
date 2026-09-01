# Examples

[简体中文](examples.zh-CN.md) | [Docs Index](README.md)

## Example 1: Add the Module to an Application

```bash
mkdir gnalloy-app && cd gnalloy-app
go mod init example.com/gnalloy-app
go get gnalloy.org/codec-socks@dev
go doc gnalloy.org/codec-socks
```

## Example 2: Inspect Current Packages

The current source tree exposes these package import paths:
- `gnalloy.org/codec-socks`

Use `go doc` against the package that matches the behavior you need:

```bash
go doc gnalloy.org/codec-socks
```

Selected current exported entry points:
- `const Version4 byte = 0x04 ...`
- `const MethodNoAuth byte = 0x00 ...`
- `const CommandConnect byte = 0x01 ...`
- `const AddressIPv4 byte = 0x01 ...`
- `const AuthVersionUserPassword byte = 0x01 ...`
- `var ErrInvalidFrame = errors.New("gnalloy/codec/socks: invalid frame") ...`

## Example 3: Use Executable Tests as Behavioral Examples

Repository tests are executable examples of supported behavior. Start with the selected names below, then read the matching `_test.go` files for complete setup and assertions. See [Testing and Performance](testing.md) for the complete discovered list.

```bash
GOWORK=off GOTOOLCHAIN=local go test ./... -run Test -count=1
```

Selected current test, benchmark, fuzz, and example entry points:
- `TestCommandReplyDecodeIPv4`
- `TestCommandRequestDecodeEncodeDomain`
- `TestCommandRequestHelpers`
- `TestGreetingDecodeEncode`
- `TestPrivateAuthResponseDecodeEncode`
- `TestSOCKS4RequestEncodeAndReplyDecode`
- `TestUsernamePasswordAuthDecodeEncode`
- `TestUsernamePasswordAuthResponseDecodeEncode`

## Example 4: Cross-Module Assembly

Direct Gnalloy dependencies for this module:
- `gnalloy.org/gnalloy`

Assembly guidance:
- Use this codec above a byte-oriented or datagram transport and below application handlers.
- The codec converts bytes or Gnalloy messages into protocol objects and converts outbound protocol objects back to bytes.
- It does not open sockets, own EventLoops, or define application lifecycle.

## Example 5: Pressure-Test Harness

For sustained load, wire this module into a scenario under `gnalloy.org/benchmarks` or a runnable client under `gnalloy.org/examples` when the module participates in network traffic. Record host, OS, CPU, Go version, protocol, payload, concurrency, warmup, repetitions, throughput, and p99 latency in the report.

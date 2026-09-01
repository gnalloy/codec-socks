# API Reference

[简体中文](api.zh-CN.md) | [Docs Index](README.md)

This inventory is generated from `go doc -short` for the packages in this repository. It is a quick public-surface map; source files and tests remain the authority for exact semantics.

## Packages

### `gnalloy.org/codec-socks`

Package name: `socks`

```text
const Version4 byte = 0x04 ...
const MethodNoAuth byte = 0x00 ...
const CommandConnect byte = 0x01 ...
const AddressIPv4 byte = 0x01 ...
const AuthVersionUserPassword byte = 0x01 ...
var ErrInvalidFrame = errors.New("gnalloy/codec/socks: invalid frame") ...
func IsPrivateMethod(method byte) bool
type CommandDecoder struct{ ... }
    func NewCommandReplyDecoder() *CommandDecoder
    func NewCommandRequestDecoder() *CommandDecoder
type CommandReply struct{ ... }
type CommandReplyEncoder struct{}
    func NewCommandReplyEncoder() *CommandReplyEncoder
type CommandRequest struct{ ... }
    func NewBindRequest(address string) CommandRequest
    func NewCommandRequest(command byte, address string) CommandRequest
    func NewConnectRequest(address string) CommandRequest
    func NewUDPAssociateRequest(address string) CommandRequest
type CommandRequestEncoder struct{}
    func NewCommandRequestEncoder() *CommandRequestEncoder
type Greeting struct{ ... }
type GreetingDecoder struct{ ... }
    func NewGreetingDecoder() *GreetingDecoder
type GreetingEncoder struct{}
    func NewGreetingEncoder() *GreetingEncoder
type MethodSelection struct{ ... }
type MethodSelectionDecoder struct{ ... }
    func NewMethodSelectionDecoder() *MethodSelectionDecoder
type MethodSelectionEncoder struct{}
    func NewMethodSelectionEncoder() *MethodSelectionEncoder
type PrivateAuthResponse struct{ ... }
type PrivateAuthResponseDecoder struct{ ... }
    func NewPrivateAuthResponseDecoder() *PrivateAuthResponseDecoder
type PrivateAuthResponseEncoder struct{}
    func NewPrivateAuthResponseEncoder() *PrivateAuthResponseEncoder
type SOCKS4Reply struct{ ... }
type SOCKS4ReplyDecoder struct{ ... }
    func NewSOCKS4ReplyDecoder() *SOCKS4ReplyDecoder
type SOCKS4Request struct{ ... }
type SOCKS4RequestEncoder struct{}
    func NewSOCKS4RequestEncoder() *SOCKS4RequestEncoder
type UsernamePasswordAuthRequest struct{ ... }
type UsernamePasswordAuthRequestDecoder struct{ ... }
    func NewUsernamePasswordAuthRequestDecoder() *UsernamePasswordAuthRequestDecoder
type UsernamePasswordAuthRequestEncoder struct{}
    func NewUsernamePasswordAuthRequestEncoder() *UsernamePasswordAuthRequestEncoder
type UsernamePasswordAuthResponse struct{ ... }
type UsernamePasswordAuthResponseDecoder struct{ ... }
    func NewUsernamePasswordAuthResponseDecoder() *UsernamePasswordAuthResponseDecoder
type UsernamePasswordAuthResponseEncoder struct{}
    func NewUsernamePasswordAuthResponseEncoder() *UsernamePasswordAuthResponseEncoder
```

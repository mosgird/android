# Mosgird android

Android application for the Mosgird protocol. The specification is in mosgird/protocols.

**Status:** not started. No code yet.

**License:** Mulan Permissive Software License, Version 2 (Mulan PSL v2). See [LICENSE.md](LICENSE.md).

## Specification

The protocol is specified in [mosgird/protocols](https://github.com/mosgird/protocols). This repository implements that specification. When the two disagree, the specification wins, and the difference is a bug to fix here or a change to propose there. Users and developers should read the specification before relying on any behavior of this software.

## What the app does

The protocol has no server and uses no domain names ([decision 0005](https://github.com/mosgird/protocols/blob/main/spec/decisions/0005-serverless-online-only-delivery.md), proposed). The app is therefore the whole system on the user's side. It holds the user's keys, encrypts and decrypts, delivers ciphertext directly to other devices while both are reachable, and keeps undelivered ciphertext until it is delivered.

On Android this has two consequences:

- **No push service.** The app does not use Firebase Cloud Messaging or any other push service to wake up. A push service is a server in the delivery path, which decision 0005 excludes, and it would learn when messages arrive.
- **Reachability depends on background limits.** Android restricts background networking (Doze and app standby), so the app is often unreachable while it is not in use. Push services are excluded ([decision 0008](https://github.com/mosgird/protocols/blob/main/spec/decisions/0008-no-push-services.md)). How a device stays reachable without them is open in the specification ([open question 17](https://github.com/mosgird/protocols/blob/main/spec/v0.1/open-questions.md#17-mobile-reachability-without-push-services)). The app adds no workaround until the specification decides.

The transport, the group protocol, and moderation are still open in the specification. This app implements none of them until they are decided there.


## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Rules for AI tools and agents are in the protocol repository.

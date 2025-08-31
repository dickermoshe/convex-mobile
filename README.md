A fork of the convex rust client for use with dart.
This fork does not modify any functional parts of the client. 
This fork only replaces `uniffi` with `flutter_rust_bridge` to 
create better dart<>rust bindings for the convex client. 

---

# Convex Mobile Libraries

This repo contains code for building mobile libraries for Convex.

The layout is as follows:

1. `rust/` - contains the wrapper around `convex-rs` that exposes types for use via FFI
2. [`android/`](android/) - contains the code for the `android-convexmobile` library
3. `ios/` - a subrepo pointing to [convex-swift](https://github.com/get-convex/convex-swift)
4. `app_for_test/` - a Convex application used for integration tests
5. `demos/` - various demos and samples to show how to use the libraries

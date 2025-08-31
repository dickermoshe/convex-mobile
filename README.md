A fork of the convex rust client for use with dart.
Very minor modifications were made to the rust client to make it work with `flutter_rust_bridge`.

1. Remove `uniffi` from the dependencies and replace it with `flutter_rust_bridge`.
1. Replace the `QuerySubscriber` trait with a struct.
2. Create a method on the `QuerySubscriber` struct to create a `Arc<QuerySubscriber>` which can be used to create a subscription from the dart side.
3. Subscribing now returns a `WrappedSubscriptionHandle` which contains a `Arc<SubscriptionHandle>` instead of returning a raw `Arc<SubscriptionHandle>` directly.

---

# Convex Mobile Libraries

This repo contains code for building mobile libraries for Convex.

The layout is as follows:

1. `rust/` - contains the wrapper around `convex-rs` that exposes types for use via FFI
2. [`android/`](android/) - contains the code for the `android-convexmobile` library
3. `ios/` - a subrepo pointing to [convex-swift](https://github.com/get-convex/convex-swift)
4. `app_for_test/` - a Convex application used for integration tests
5. `demos/` - various demos and samples to show how to use the libraries

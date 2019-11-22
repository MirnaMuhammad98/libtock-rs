# Releases

## 0.2.0 (WIP)

- Many functions, including `main()` are asynchronous
  - To retrieve the value of an asynchronous `value`, use `value.await`
  - This is only possible within an `async fn`, so either
    - Make the caller `fn` of `.await` an `async fn`
    - Not recommended: Use `core::executor::block_on(value)` to retrieve the `value`
- `syscalls::yieldk_for` is no longer available
  - Yielding manually is discouraged as it conflicts with Rust's safety guarantees. If you need to wait for a condition, use `futures::wait_until` and `.await`.

## a8bb4fa9be504517d5533511fd8e607ea61f1750 (0.1.0)

- First and highly experimental `libtock-rs` API
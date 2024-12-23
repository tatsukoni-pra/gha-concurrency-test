## 挙動メモ

```yml
concurrency:
  group: test_job
  cancel-in-progress: false
```

- Test Job を重複実行する：
　- 最新の実行は待機する。それ以外はキャンセル扱いになる
- Test Job 1 を実行後、間髪入れずにTest Job 2 を実行する
　- Test Job 1・Test Job 2 の両方が実行される

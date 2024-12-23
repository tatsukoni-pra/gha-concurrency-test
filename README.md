## 挙動メモ

### 記述例1

```yml
concurrency:
  group: test_job
  cancel-in-progress: false
```

### 結果

- Test-Job を重複実行する：
　- 最新の実行は待機する。それ以外はキャンセル扱いになる
- Test-Job を実行後、間髪入れずにTest-Job-2 を実行する
　- Test-Job・Test-Job-2 の両方が実行される

### 記述例2

```yml
concurrency: test_job
```

### 結果

- 記述例1と結果変わらず

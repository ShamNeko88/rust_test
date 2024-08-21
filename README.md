# Rust!!!

### Cargoとは
- Rustのビルドシステム兼パッケージマネージャー
- プロジェクトの依存関係の管理やビルドプロセスの容易に行うことができる
***

### Cargoで新しいプロジェクトの開始
```powershell
cargo new [プロジェクト名]
cd [プロジェクト名]
cargo build
cargo run
```
***

### Cargoでフォーマット
```powershell
cargo fmt
```
***

### Cargoでテスト
- #[cfg(test)] と #[test] アトリビュートでテスト関数を定義
```rust
// main.rs

#[cfg(test)]

mod tests {
    #[test]
    fn it_works() {
        assert_eq!(2 + 2, 4);
    }
}
```

- 下記コマンドでテスト実行
```powershell
cargo test
```
***

### Clippyで静的解析
```powershell
cargo clippy
```

### コンパイル
- hello_world.rs ファイルのコンパイル
- プロジェクトルート配下にファイル作成し、下記コマンド実行
```powershell
rustc hello_world.rs
```
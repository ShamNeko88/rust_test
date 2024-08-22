# Rust!!!

###### Cargoとは
- Rustのビルドシステム兼パッケージマネージャー
- プロジェクトの依存関係の管理やビルドプロセスの容易に行うことができる
***

### フォーマット
###### Cargoでフォーマット
- ファイルを直接フォーマットしてくれる
```powershell
cargo fmt
```
***

### テスト
###### Cargoでテスト
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

### 静的解析
###### Clippyで静的解析
```powershell
cargo clippy
```

###### Cargo.toml
- Cargoプロジェクトの設定ファイル
- 下記情報が含まれる
  1. プロジェクトのメタデータ（名前、バージョン、著者など）
  2. プロジェクトの依存関係
- [package] セクション
  - プロジェクト名
  - バージョン
  - 著者
  - etc...
- [dependencies] セクション
  - プロジェクトの依存関係
  - 必要なライブラリ
```toml
[package]
name = "try_rust"
version = "0.1.0"
authors = ["Unknown <unknown@example.com>"]
edition = "2021"

[dependencies]
```
***

### コンパイル
- rustc
  - 簡易コンパイル
- cargo build
  - プロジェクト全体のコンパイル

###### rustcによるコンパイル
- 例としてhello_world.rs ファイルのコンパイル
- プロジェクトルート配下にファイル作成し、下記コマンド実行
```powershell
rustc hello_world.rs
```

###### cargoによるコンパイル
- プロジェクトを丸々コンパイル
- プロジェクトルート配下で下記を実行
- 「target/debug」配下にバイナリを生成
```powershell
cargo build
```
***
### 実行
- コンパイルから実行まで一括で行う
```powershell
cargo run
```
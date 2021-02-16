# Chap2. The Structure of the Java Virtual Machine

## 2.1 The class File Format
* JVMで実行されるコードはclass file formatで表現されている.
* class file formatの詳細は4章で説明.

## 2.2 Data Types
* JVMにはprimitive型とreference型がある
* primitive型ごとに命令がある: e.g.) iadd, ladd, fadd, dadd
* JVMはobjectを明示的にサポート. オブジェクトを指す値がreference型.

## 2.9 Special Methods
* Initialization methodなど
* `<init>`
* `<clinit>`

## 2.12 Public Design, Private Implementation
* 仕様(public design)に従っていれば，実装(private implementation)は自由に行って良い
  - 今まで扱ってきた「仕様」は"クラスファイルの形式"と"命令セット"
  - JITをしたり，というのは「実装」の世界の話

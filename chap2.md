# Chap2. The Structure of the Java Virtual Machine

## 2.9 Special Methods
* Initialization methodなど
* <init>
* <clinit>

# 2.12 Public Design, Private Implementation
* 仕様(public design)に従っていれば，実装(private implementation)は自由に行って良い
  - 今まで扱ってきた「仕様」は"クラスファイルの形式"と"命令セット"
  - JITをしたり，というのは「実装」の世界の話

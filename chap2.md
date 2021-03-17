# Chap2. The Structure of the Java Virtual Machine

## 2.1 The class File Format
* JVMで実行されるコードはclass file formatで表現されている.
* class file formatの詳細は4章で説明.

## 2.2 Data Types
* JVMにはprimitive型とreference型がある
* primitive型ごとに命令がある: e.g.) iadd, ladd, fadd, dadd
* JVMはobjectを明示的にサポート. オブジェクトを指す値がreference型.

## 2.3 Primitive Types and Values
* numeric types
  - integral types
    + byte
    + short
    + int
    + long
    + char
  - floating-point types
    + float
    + double
  - boolean type
  - returnAddress type
    + returnAddress 型のみ直接にJava言語の型と対応づいていない．

## 2.4 Reference Types and Values
* Reference Typesは以下の３つ
  - class types
  - array types
  - interface types
* Array型(wIP)
* Reference valueはnullを取ることがあり．
* Null値が具体的なencodingはJVMの仕様書で規定せず

## 2.5 Run-Time Data Areas

### 2.5.1 The pc Register
* JVMは同時に複数のスレッドを実行できる
* スレッドは各自pc(program counter)レジスタを持つ
* nativeメソッドでなければ，pcレジスタはJVMの命令のアドレスを持つ
* nativeメソッドなら，pcレジスタはundefined
* JVMのpcレジスタは十分にwideなので，returnAddressや特定の環境のnativeポインタも保持できる.

### 2.5.2 Java Virtual Machine Stacks
* スレッドごとにスタックがある

### 2.5.3 Heap

### 2.5.4 Method Area

### 2.5.5 Run-Time Constant Pool

### 2.5.6 Native Method Stacks

## 2.9 Special Methods
* Initialization methodなど
* `<init>`
* `<clinit>`

## 2.12 Public Design, Private Implementation
* 仕様(public design)に従っていれば，実装(private implementation)は自由に行って良い
  - 今まで扱ってきた「仕様」は"クラスファイルの形式"と"命令セット"
  - JITをしたり，というのは「実装」の世界の話

[Elixir をインストール](https://elixir-lang.jp/install.html) のページを見よ、とある。MacPorts からでもインストールできるようだ。Ports から入れられる時にはまず info を読む、でしょう?
```
% port info elixir
elixir @1.10.3 (lang)

Description:          Elixir is a functional, meta-programming aware language built on top
                      of the Erlang VM. It is a dynamic language that focuses on tooling to
                      leverage Erlang's abilities to build concurrent, distributed and
                      fault-tolerant applications with hot code upgrades.
Homepage:             http://elixir-lang.org/

Library Dependencies: erlang
Conflicts with:       arb
Platforms:            darwin
License:              Apache-2
Maintainers:          Email: me@milmazz.uno, GitHub: milmazz
                      Email: ciserlohn@macports.org, GitHub: ci42
```
ついで variants も確認する、でしょう?
```
% port variants elixir
elixir has no variants
```
なにもなかったですね。ではインストール。
```
% sudo port install elixir
--->  Computing dependencies for elixir
The following dependencies will be installed:  erlang
Continue? [Y/n]: Y
--->  Fetching archive for erlang
(snip)
--->  Installing elixir @1.10.3_0
--->  Activating elixir @1.10.3_0
--->  Cleaning elixir
--->  Updating database of binaries
--->  Scanning binaries for linking errors
--->  No broken files found.
--->  No broken ports found.
```
確認してみましょう。
```
% rehash
% elixir --version
Erlang/OTP 23 [erts-11.0] [source] [64-bit] [smp:8:8] [ds:8:8:10] [async-threads:1] [hipe]

Elixir 1.10.3 (compiled with Erlang/OTP 23)
```
ログは GitHub で記述することにして、ElixirTutorial というリポジトリを web UI で作成しました。そのリポジトリを clone してサンプルプログラムなどをここに格納することにしましょう。
```
% cd ~/Documents/source
% git clone git@github.com:reokashiwa/ElixirTutorial.git
Cloning into 'ElixirTutorial'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), 4.51 KiB | 4.51 MiB/s, done.
```
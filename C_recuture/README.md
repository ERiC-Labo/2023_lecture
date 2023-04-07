# C_recture_2023

C_rinという名前のフォルダを作り、**各週のフォルダや各演習のファイルは分けて**、見やすいようにしましょう。<br>以下は、ターミナル上でのフォルダ作成や移動のコマンドです。<br>**コマンドは多様にあるので、自分で調べるようにしましょう。** ←とても大事
```
mkdir C_rin #C_rinという名前のフォルダを作る
cd C_rin　#C_rinに移動
mkdir week1
cd week1 
code ./ #今の開いていいる場所のVCcodeを開く
```
各週の演習問題は[Atcoder](https://atcoder.jp/contests/APG4b/tasks)の練習問題を使用します。指定された問題に取り組みましょう。
<br>出力はターミナルで行えるようにしましょう。

# 出力の流れ
1.フォルダ作成　（上に書いてあります）
<br>2.コード書き込む
<br>3.コンパイル（C++では必要です）
　主にウェブサイトとでは、g++を使ってコンパイルしていますが、cmakeを使ってください。<br>以下は実装例です。ただし、week1内で行ってください。
 ```
touch CMakeLists.txt 
```
CMakeList内に以下を書き込みます。自分で変更する箇所に注意しましょう。
 ```
cmake_minimum_required(VERSION 3.13)

# プロジェクトの情報
project(”自分で適当に名前決める”)

##実行ファイル名を設定
add_executable(
    ${PROJECT_NAME} sato.cpp #←sato.cppは実行するファイル名
)
 
##リンクするライブラリを読み込む
target_link_libraries(
    ${PROJECT_NAME} 
)
```
次に、buildフォルダ作成し、移動します。
```
mkdir build
cd build
cmake .. 
make #ビルド完了
```

4.実行
```
./${PROJECT_NAME} 
```


# 今週のテーマOpenCVを使おう
# STEP 1 : 画像を表示してみよう

OpenCVは画像を簡単に扱うことができるライブラリです。画像輪講もターミナルで実行してください。
<br>はじめに、画像を表示するコードを書いてみましょう。<br>画像は上のinput_imageというフォルダにあるものを画像輪講用に作ったフォルダ内に保存して、使用して下さい。<br>また、画像の表示は以下のコードを参考にしてくだい。

~~~cpp
#include <opencv2/opencv.hpp>

int main()
{
    // image.pngをimgに代入
    cv::Mat img = cv::imread("画像のパス");

    // imgの表示
    cv::imshow("img", img);

    // キーが押されるまで待機
    cv::waitKey(0);

    return 0;
}
~~~
以上のコードをC++ファイルに書きましょう。<br>・cv::Matとは、画像を保存できる変数の型です。
<br>・cv::imreadという関数で、画像ファイルをcv::Matへ変換します。実行場所から画像への相対パスを引数に持ちます。
<br>・cv::imshowという関数で、cv::Matを表示することができます。

<br>次に、以下のコードをCMakeListsに書き、C輪講同様にコンパイルし、実行しましょう。

```
cmake_minimum_required(VERSION 2.8.3)
project(step1)
set(SOURCE_FILE main.cpp)

# OpenCVのビルド環境の設定ファイルを読み込む
find_package(OpenCV REQUIRED)

# OpenCV関係のインクルードディレクトリのパスを設定
include_directories(
    ${OpenCV_INCLUDE_DIRS}
)

# 実行ファイル名を設定
add_executable(main
    ${SOURCE_FILE}
)

# リンクするライブラリを読み込む
target_link_libraries(main
    ${OpenCV_LIBRARIES}
)
```


# STEP2:画像を白黒にしてみよう
```
#include <opencv2/opencv.hpp>

int main()
{
    // image.pngをimgに代入
    cv::Mat img = cv::imread("../image.jpg");

    // imgを白黒にしてimg_binに代入
    cv::Mat img_bin;
    cv::cvtColor(img, img_bin, cv::COLOR_BGR2GRAY);

    // imgの表示
    cv::imshow("img_bin", img_bin);

    // キーが押されるまで待機
    cv::waitKey(0);

    return 0;
}
```
・cv::cvtColorとは、画像の色を別の形式へ変換するものです。元の画像、変換後の画像、変換方法の3つを引数に取ります。

# STEP 3 : 直線を検出してみよう
色を変更することにとどまらず、OpenCVを使えば様々なことが関数1つでできます。ここでは、画像から直線を検出してみましょう。<br>まずは、Canny法によるエッジ検出をしてみます。たった1行で書けます。コピペでも可ですがこのままだとエラーが出るので、エラーを読み自分で解決してみましょう！（img_cannyという変数は用意しましたか？？）
```
cv::Canny(img, img_canny, 500.0, 700.0);
```
cv::CannyでCanny法によるエッジ検出ができます。元画像、出力画像、閾値2つ、の計4つの引数を持ちます。
[cv::Cannyの公式ドキュメント](https://docs.opencv.org/4.x/dd/d1a/group__imgproc__feature.html#ga04723e007ed888ddf11d9ba04e2232de)

<br>**本日はここまでですが、余力のある人はSTPE４に進んでください。**
<br>**STEP4 ： pythonで書き換えよう**
今日のSTEP１~3までをpythonで書き換えてみましょう。<br>研究では,pythonも使うのでなれておきましょう！[参考サイト](https://algorithm.joho.info/programming/python/c-language-kijutsu-hikaku-chigai/#toc2)


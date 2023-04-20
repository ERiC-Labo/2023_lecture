# 今週のテーマ:２値化や多値化

# 単純な2値化
input_imgのimg1とimg2について閾値を自分で決め、適切な2値化を考えてみましょう。<br>
処理した画像の名前をbinary_img1.jpg,binary_img2.jpgと名付け、保存しましょう。<br>
（カラー画像はグレースケールが有効です）
# 大津の2値化
input_imgのimg1とimg2について、大津の2値化を適用し、otu_img1.jpg,otu_img2.jpgと名付けましょう<br>
そして、binary_img1.jpgとotu_img1.jpgを横に結合して表示し、concat_img.jpgという名前で保存しましょう。<br>
見比べたのち、ノイズが少ない画像に対して、ノイズ除去を行いclear_img.jpgという名前で保存して下さい。

。手法は問いません。<br>
# 3値化
input_imgのimg3について適切な3値化を行い、triangulated_imgという名前で保存しましょう。<br>br

# 確認
以上のSTEPを終えると、<br>
・binary_img1.jpg<br>
・binary_img2.jpg<br>
・otu_img1.jpg<br>
・otu_img2.jpg<br>
・concat.jpg<br>
・clear_img.jpg<br>
・triangulated_img<br>
以上の７枚の画像が保存されていると思います。先輩に７枚の画像を確認してもらい、演習は終了です。

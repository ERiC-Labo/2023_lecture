# 今週のテーマ:２値化と多値化

# STEP1:単純な2値化
input_imgのimg1とimg2について閾値を自分で決め、適切な2値化を考えてみましょう。<br>
img1に処理した画像の名前をbinary_img1.jpg,binary_img2.jpgと名付け、保存しましょう。<br>
何度か閾値を変更して、いい塩梅の画像を見つけましょう。

# STP2:大津の2値化
input_imgのimg1とimg2について、大津の2値化を適用し、otu_img1.jpg,otu_img2.jpgと名付けましょう<br>
そして、binary_img1.jpgとotu_img1.jpgを横に結合して表示し、concat_img.jpgという名前で保存しまし<br>
ノイズ除去の手法は問いません。<br>

# STEP3:3値化
input_imgのimg3について適切な3値化を行い、triangulated_img.jpgという名前で保存しましょう。<br>
さらに、img3について適切な5値化を行い、pentanalized_img.jpgという名前で保存しましょう。<br>


# 確認
以上のSTEPを終えると、<br>
・binary_img1.jpg<br>
・binary_img2.jpg<br>
・otu_img1.jpg<br>
・otu_img2.jpg<br>
・concat.jpg<br>
・clear_img.jpg<br>
・triangulated_img.jpg<br>
・pentanalized_img.jpg<br>
以上の8枚の画像が保存されていると思います。先輩に8枚の画像を確認してもらい、演習は終了です。

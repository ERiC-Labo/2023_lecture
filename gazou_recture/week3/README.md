# 今週のテーマ:２値化と多値化

# STEP1:単純な2値化
input_imgのimg1とimg2について閾値を自分で決め、適切な2値化を考えてみましょう。<br>
２値化処理した画像の名前をそれぞれbinary_img1.jpg,binary_img2.jpgという名前で保存しましょう。<br>
何度か閾値を変更して、いい塩梅の画像を見つけましょう。（画像内の対象物に意味付けをする）

# STP2:大津の2値化
input_imgのimg1とimg2について、大津の2値化を適用し、otu_img1.jpg,otu_img2.jpgと名付けましょう<br>
そして、binary_img1.jpgとotu_img1.jpgを横に結合して表示し、concat1_img.jpgという名前で保存しましょう<br>
さらに、binary_img2.jpgとotu_img2.jpgを横に結合して表示し、concat2_img.jpgという名前で保存しましょう<br>
どのような画像にて、大津の２値化は有効ではないのでしょうか。

# STEP3:多値化
input_imgのimg3について適切な3値化を行い、triangulated_img.pngという名前で保存しましょう。<br>
さらに、img3について適切な5値化を行い、pentanalized_img.pngという名前で保存しましょう。<br>


# 確認
以上のSTEPを終えると、<br>
・binary_img1.jpg, binary_img2.jpg<br>
・otu_img1.jpg, otu_img2.jpg<br>
・concat1_img.jpg, concat2_img.jpg<br>
・triangulated_img.png , pentanalized_img.png<br>
以上の8枚の画像が保存されていると思います。先輩に8枚の画像を確認してもらい、演習は終了です。

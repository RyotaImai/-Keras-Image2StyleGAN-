# [Keras]Image2StyleGAN++
# これは何？
Image2StyleGAN++(https://arxiv.org/abs/1911.11544) をKerasで実装してみました。  
ラボで使いまわすようなのでassertとか何も書いてないです。気が向いたらそこらへん整備します...  
ノイズ最適化はまだ未実装です。そのうちやります。  
## [環境]
Cuda 10.1  
GPU  NVIDIA Tesla P-100  
Driver : 418.87.01
## [Python Requirement]
Keras==2.3.1  
tensorflow-gpu==1.15.0  
[こちら](https://github.com/RyotaImai/StyleGAN_Picke2Keras "StyleGAN_Picke2Keras")のリポジトリもクローンしてください  

## [使い方]
1. お好きなStyleGANのpklファイルを上のリポジトリ内のコンバータでh5に変換してください。
2. Configのところは基本そのままで大丈夫です。GANの出力が224以下の時適当な値に修正してください。
```
VGG_INPUT = 224
```
3. 自分の環境に合わせて埋めてください
```
target_image_path   = "IMG_2791.jpg"
weights_path        = "-----.h5"
save_image_path     = "IMG_2791/"
save_image_name     = "IMG_2791"
save_latent_path    = "IMG_2791_dlatent.npy"
res = 1024
stage = 18
```
4. あとは全部実行するだけ!!!　　
Elle Fanningのお顔を借りております。。。  
左 : オリジナル
右 : embedding後の画像  
<img src="https://github.com/RyotaImai/-Keras-Image2StyleGAN-/blob/master/md_images/Elle-faning%20(2).jpg" width=50%><img src="https://github.com/RyotaImai/-Keras-Image2StyleGAN-/blob/master/md_images/Elle(2)_5000.jpg" width=50%>

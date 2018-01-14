clear; % 変数のオールクリア

ORG=imread('himawari.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

pause;

imhist(ORG); % ヒストグラムの表示

![1](https://user-images.githubusercontent.com/32251471/34913204-15ad872a-f93a-11e7-9781-e4938adf45bc.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34913207-188611f6-f93a-11e7-90f7-f7f474cbd967.PNG)

図2　ヒストグラム

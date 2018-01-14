clear; % 変数のオールクリア

ORG=imread('Lenna.png'); % 原画像の入力

ORG = rgb2gray(ORG);

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause; % 一時停止


IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![1](https://user-images.githubusercontent.com/32251471/34913295-5507da2c-f93c-11e7-905e-63e472fc6544.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34913296-56fa66ce-f93c-11e7-8c50-b486edcd5230.PNG)

図2　128による二値化画像

![3](https://user-images.githubusercontent.com/32251471/34913297-591e8944-f93c-11e7-875a-15287a03156e.PNG)

図3　ディザ法による二値化画像

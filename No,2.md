clear; % 変数のオールクリア

ORG=imread('himawari.jpg'); % 原画像の入力

ORG = rgb2gray(ORG); colormap(gray); colorbar;

imagesc(ORG); axis image; % 画像の表示

pause; % 一時停止

% ２階調画像の生成

IMG = ORG>128; 

imagesc(IMG); colormap(gray); colorbar;  axis image;

pause;

% ４階調画像の生成

IMG0 = ORG>64;

IMG1 = ORG>128;

IMG2 = ORG>192;

IMG = IMG0 + IMG1 + IMG2; %384

imagesc(IMG); colormap(gray); colorbar;  axis image;

%　８階調画像の生成

IMG0 = ORG>32;

IMG1 = ORG>64;

IMG2 = ORG>96;

IMG3 = ORG>128;

IMG = IMG0 + IMG1 + IMG2 + IMG3; %418

imagesc(IMG); colormap(gray); colorbar;  axis image;


![1](https://user-images.githubusercontent.com/32251471/34907582-69d6be6e-f8c4-11e7-94b8-0d3ffe69e0bb.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34907588-79fef068-f8c4-11e7-9c2d-734115f83dd8.PNG)

図2　2階調画像の生成

![3](https://user-images.githubusercontent.com/32251471/34907590-801e32ce-f8c4-11e7-9978-62c17fd82511.PNG)

図3　4階調画像の生成

![4](https://user-images.githubusercontent.com/32251471/34907592-865b3a88-f8c4-11e7-886d-8e6201028d39.PNG)

図4　8階調画像の生成

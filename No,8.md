ORG = imread('himawari.jpg'); % 画像の読み込み

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

IMG = ORG > 128; % 閾値128で二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

pause;

![1](https://user-images.githubusercontent.com/32251471/34913471-82edced8-f941-11e7-9d7e-ec5e03eeced5.PNG)

図1　二値化画像

![2](https://user-images.githubusercontent.com/32251471/34913472-8614a672-f941-11e7-8aa2-0892b2230a0a.PNG)

図2　ラベル

ORG = imread('himawari.jpg'); % 画像の読み込み

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

pause;

![1](https://user-images.githubusercontent.com/32251471/34913567-867e2f68-f944-11e7-8fd8-47c978b50078.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34913568-88e52ac2-f944-11e7-80ea-2d8af82526ed.PNG)

図2　ノイズ添付画像

![3](https://user-images.githubusercontent.com/32251471/34913414-059069a6-f940-11e7-9b99-3c97e322449d.PNG)

図3　平滑化フィルタ

![4](https://user-images.githubusercontent.com/32251471/34913570-8c8c76a8-f944-11e7-8156-eae88e7bf268.PNG)

図4　メディアンフィルタ

![5](https://user-images.githubusercontent.com/32251471/34913572-8e7154de-f944-11e7-8114-d36b5db29b67.PNG)

図5　フィルタ適用


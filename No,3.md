clear; % 変数のオールクリア

ORG=imread('himawari.jpg'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示
pause;

IMG = ORG > 42; % 輝度値が42以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

IMG = ORG > 84;　% 輝度値が84以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

IMG = ORG > 126;　% 輝度値が126以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

pause;

IMG = ORG > 168;　% 輝度値が168以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![1](https://user-images.githubusercontent.com/32251471/34907686-ae077578-f8c5-11e7-805d-e9ee6af60d16.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34907689-b1e8f428-f8c5-11e7-9f10-2520f221f318.PNG)

図2　閾値42の画像

![3](https://user-images.githubusercontent.com/32251471/34907690-b48f3d72-f8c5-11e7-9729-3d38fe764a25.PNG)

図3　閾値84の画像

![4](https://user-images.githubusercontent.com/32251471/34907691-b6869a80-f8c5-11e7-80af-0ee64b1de561.PNG)

図4　閾値126の画像

![5](https://user-images.githubusercontent.com/32251471/34907692-b90fbc64-f8c5-11e7-872a-3215d7aee331.PNG)

図5　閾値168の画像

ORG = imread('himawari.jpg'); % 画像の読み込み

ORG = rgb2gray(ORG); % 白黒濃淡画像に変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

imhist(ORG); % 濃度ヒストグラムを生成、表示

pause;

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

pause;

ORG = uint8(ORG); % この行について考察せよ

imhist(ORG); % 濃度ヒストグラムを生成、表示

![1](https://user-images.githubusercontent.com/32251471/34913412-ffdcd35a-f93f-11e7-8816-66bc292e7684.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34913413-03727786-f940-11e7-8f4d-75434a9c2044.PNG)

図2　ヒストグラム

![3](https://user-images.githubusercontent.com/32251471/34913414-059069a6-f940-11e7-9b99-3c97e322449d.PNG)

図3　濃度値の最大最小値計算後の画像

![4](https://user-images.githubusercontent.com/32251471/34913415-072a92c8-f940-11e7-8238-029be8c8bc96.PNG)

図4　ヒストグラム

![5](https://user-images.githubusercontent.com/32251471/34913416-08e9dcc2-f940-11e7-9d60-58d91e857aa6.PNG)

図5　計算結果

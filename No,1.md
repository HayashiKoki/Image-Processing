ORG=imread('hana.png'); % 原画像の入力
imagesc(ORG); axis image; % 画像の表示

IMG = imresize(ORG,0.5); % 画像の縮小
IMG2 = imresize(IMG,2,'box'); % 画像の拡大
imagesc(IMG2); axis image ; % 画像の表示

IMG = imresize(IMG,0.5); % 画像の縮小
IMG2 = imresize(IMG,4,'box') % 画像の拡大
imagesc(IMG2); axis image ; % 画像の表示

IMG = imresize(IMG,0.5); % 画像の縮小
IMG2 = imresize(IMG,8,'box') % 画像の拡大
imagesc(IMG2); axis image ; % 画像の表示

![1](https://user-images.githubusercontent.com/32251471/34907541-aa20df96-f8c3-11e7-9a22-f3af52c9b039.PNG)

図1　原画像

![2](https://user-images.githubusercontent.com/32251471/34907547-bf5b3d52-f8c3-11e7-9b7e-52475612c366.PNG)

図2　1/2サンプリング画像

![3](https://user-images.githubusercontent.com/32251471/34907548-c788399e-f8c3-11e7-91a2-552e71ec54fa.PNG)

図3　1/4サンプリング画像

![4](https://user-images.githubusercontent.com/32251471/34907552-cd835162-f8c3-11e7-9565-4de8b782c8c7.PNG)

図4　1/8サンプリング画像

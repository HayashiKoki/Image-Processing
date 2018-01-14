ORG=imread('himawari.jpg'); % 原画像の入力

ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

pause;

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納

myu_T = mean(H);

max_val = 0;

max_thres = 1;

for i=1:255

C1 = H(1:i); %ヒストグラムを2つのクラスに分ける

C2 = H(i+1:256);

n1 = sum(C1); %画素数の算出

n2 = sum(C2);

myu1 = mean(C1); %平均値の算出

myu2 = mean(C2);

sigma1 = var(C1); %分散の算出

sigma2 = var(C2);

sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出

sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出

if max_val<sigma_B/sigma_w

max_val = sigma_B/sigma_w;

max_thres =i;

end;

end;

IMG = ORG > max_thres;

imagesc(IMG); colormap(gray); colorbar;

pause;

![1](https://user-images.githubusercontent.com/32251471/34913234-cd6f46d2-f93a-11e7-990f-4a469a10b0bd.PNG)

図1　グレースケール画像

![2](https://user-images.githubusercontent.com/32251471/34913237-d135de0c-f93a-11e7-86bb-ffd013287d56.PNG)

図2　二値化画像

![5 3](https://user-images.githubusercontent.com/32251471/34913238-d359c7ac-f93a-11e7-9996-d0d35ca0c02b.PNG)

図3　計算結果

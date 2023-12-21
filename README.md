# YOLOとDockerの使用について

## ステップ1：イメージのインストール

### docker pull ludiwangfpga/yolo:v7
![image](https://github.com/ludiwangfpga/ludiwangfpga/blob/main/%E5%9B%BE%E7%89%871.png#w30)

## 第二ステップ：コマンドの入力

### docker run -it  -v "/home/wang/docker/file/1.pt:/app/1.pt" -v "/home/wang/docker/file/1.mp4:/app/1.mp4" ludiwangfpga/yolo:v7 --weights /app/1.pt
事前に1.ptファイルと1.mp4ファイルを用意してください。
カメラを呼び出すためのコマンドに「--device=/dev/video0」を追加します。
-vの後には1.ptと1.mp4のファイルがあるディレクトリを指定し、ディレクトリの後に「:/app/1.pt」を追加します。
単一の画像またはフォルダ全体の画像を認識する必要がある場合は、同様にアップロードできます。

docker ps
docker exec -it 067e3044971f /bin/bash
cd runs/detect/exp/
exit
docker cp 067e3044971f:app/runs/detect/exp/1.mp4 /home/wang/docker/



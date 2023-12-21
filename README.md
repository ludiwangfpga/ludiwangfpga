
docker pull ludiwangfpga/yolo:v7
![image](https://github.com/ludiwangfpga/ludiwangfpga/blob/main/%E5%9B%BE%E7%89%871.png)


docker run -it --device=/dev/video0 -v "/home/wang/docker/file/1.pt:/app/1.pt" -v "/home/wang/docker/file/1.mp4:/app/1.mp4" ludiwangfpga/yolo:v7 --weights /app/1.pt
docker ps
docker exec -it 067e3044971f /bin/bash
cd runs/detect/exp/
exit
docker cp 067e3044971f:app/runs/detect/exp/1.mp4 /home/wang/docker/



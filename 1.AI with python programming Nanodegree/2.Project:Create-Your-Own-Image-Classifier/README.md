--sanity-check


![Screenshot (285)](https://github.com/Yasmeen-Begum/Udacity/assets/91931504/cc7811f3-91be-4338-bee1-bfd9ad205108)


--predicting the image

![Screenshot (286)](https://github.com/Yasmeen-Begum/Udacity/assets/91931504/60d6ca30-2f84-4704-9d36-cd68a4aa5d38)

![Screenshot (287)](https://github.com/Yasmeen-Begum/Udacity/assets/91931504/0f4dfc19-8cb6-40f9-a1d7-6c773f4ff110)


--for train.py

python train.py flowers --learning_rate 0.01 --epochs 5

Train Loss: 4.43

Valid Loss: 4.22

Accuracy: 10.88%

model saved to ../saved_models/checkpoint.pth

--For predict.py

python predict.py './flowers/test/63/image_05882.jpg' --top_k 5 '../saved_models/checkpoint.pth'  --gpu

Predictions:

#0   petunia                   Prob: 2.73%

#1   rose                      Prob: 2.16%

#2   water lily                Prob: 1.96%

#3   lotus lotus               Prob: 1.90%

#4   cyclamen                  Prob: 1.81%

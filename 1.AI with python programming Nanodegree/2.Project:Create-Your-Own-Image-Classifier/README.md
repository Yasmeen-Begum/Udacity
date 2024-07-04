--sanity-check

![Screenshot (285)](https://github.com/Yasmeen-Begum/Create-Your-Own-Image-Classifier/assets/91931504/f8ba3e3f-4d7b-4709-b748-1a4ee4952e5b)

--predicting the image

![Screenshot (284)](https://github.com/Yasmeen-Begum/Create-Your-Own-Image-Classifier/assets/91931504/4f0a46ac-39b2-4c6d-9efc-5f6e4784d84a)


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

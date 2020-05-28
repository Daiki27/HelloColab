# HelloColab
[1] 2020.5.29

#Colaboratoryとgithubの連携について.

## やりたい事
Colaboratoryのコードをgitにpushして, gitで管理したい.

## 問題
1. Colaboratory上でipynbをpushできるが, 差分管理がipynb形式なので辛い.

2. Colaboratory上でipynbをpyに変換して, それをpushしようとした. しかし, 以下のコマンドの出力はtxtだった.
  
  - jupyter nbconvert --to script *.ipynb
  - これの原因は, おそらくpyに変換するためのデータがipynbに含まれていないはず.
  - https://stackoverflow.com/questions/48568388/nbconvert-suddenly-producing-txt-instead-of-py
  
3. そこでColaboratory上のメニュータブで「.pyに保存」をして, ローカル環境(デスクトップ)に保存.

4. 保存したファイルからターミナルでgitにpushをした. それをColaboratory上で操作したい.

5. しかし, Colaboratory上でpyファイルを単純には読み込みなかった.


## 当座の解決策

1. Colaboratory上のメニュータブで「.pyに保存」「.ipynbに保存」をして, ローカル環境(デスクトップ)に保存.

2. ターミナルでローカルの「.py」「.ipynb」を共にgitにpushをする.

3. Colaboratory上で開く時には, 「.ipynb」を開いて編集・保存をする.

4. 1に戻る.

5. 注意点：gitでipynbを見ようとすると, “Sorry, something went wrong. Reload?”, となり見れない.
  

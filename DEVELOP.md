### exe化 (windows用)
```
cd MicroscopeController
pyinstaller .\run.py -F -w --icon=.\presentation\img\icon.ico --add-data "settings;settings" --add-data "presentation;presentation"
cp .\presentation, .\settings .\dist -Recurse 
```
MicroscopeController\dist\run.exe に実行ファイルが生成される

### pythonでの実行
- 実環境: ```python .\run.py```
- mock環境: ```python .\run.py --mock```

### 現在のバグ
- コントローラが正しく接続されていない状態で起動するとフリーズする
- feature_matchおよびphase_matchでのマッチングでエラーが発生することがある
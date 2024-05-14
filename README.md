# Video Processing Server
このプロジェクトは、ビデオファイルを処理するためのサーバーアプリケーションです。サーバーはTCP接続を介してクライアントからビデオファイルを受信し、指定された操作（圧縮、解像度変更、アスペクト比変更、MP3抽出、GIFまたはWebMへの変換）を実行します。処理が完了すると、サーバーは結果をクライアントに送信します。

### 機能
- ビデオファイルの圧縮
- 解像度の変更
- アスペクト比の変更
- ビデオからのMP3抽出
- ビデオをGIFまたはWebMに変換
- 動画の一部を切り取り変換

### セットアップ
```
sudo apt-get install python3-tk
sudo apt-get install ffmpeg
```
### 実行ディレクトリ
```
recursion-training/VideoCompressor/VideoCompressor/
client.py、7行目のFILE_PATHにて、使用するMP4ファイルが存在するディレクトリを指定する
デフォルトではinputフォルダ内のmp4ファイルを読み込む
```
### サーバーの起動
```
python server.py
```

### クライアントの起動
```
python client.py
```

### 使用方法
1. サーバー、クライアントの順番で起動する
2. クライアント側のターミナルでmp4ファイルを選択する
3. mp4ファイルに対しての操作を選択する（ex. 圧縮、解像度の変更など）
4. サーバー側にリクエストが送られ、成功するとoutputフォルダに編集済みのファイルが保存される
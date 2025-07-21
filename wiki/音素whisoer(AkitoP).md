### 学習コード
学習コードは公開されていない？ので再現したものが[WariHima/phoneme-whisper-ja](https://github.com/WariHima/phoneme-whisper-ja)に  

### 学習時の注意  
"[" "]"はスペシャルトークンに含まれるため"↑" "↓"に置換  
音素で学習すると出力が壊れやすいのでカタカナ（発音系）で学習  
pauは一文字の記号にしたほうが学習効率が上がるため①に置換  
先頭記号、終端記号は除く
#### 学習時のラベルそして推論時の出力の例  
`フ↑ロ↓ニ#ハ↓イッタノデ①キ↓ブンガイッ#ソ↑オ#ヨ↓クナッタ`  

### リンク
huggingface space demo  
https://huggingface.co/spaces/AkitoP/whisper-japanese-prosodic-jsut5000_only

最新の音素whisper lora  
https://huggingface.co/AkitoP/whisper-jsut5000-voicevox-phone-lora  
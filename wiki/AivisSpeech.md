## 概要
AivisSpeechは[aivis-project](https://aivis-project.com/)の[tsukumijima氏](https://github.com/tsukumijima)が開発しているVoiceVoxをベースにした音声合成ソフトである。


### ダウンロード
[公式サイト](https://aivis-project.com/)もしくは[githubのリリース](https://github.com/Aivis-Project/AivisSpeech/releases)からダウンロ－ド出来る


### 公表されていない独自機能
AivisSpeech自体がossのため、またモデルの学習環境もあることから、大企業(DMM)などが使用する恐れがあるため、向上した点は公表されていない。

#### pyopenjtalk-plusを使用
g2pライブラリにpyopenjtalk各forkをマージしたpyopenjtalk-plusを使用している。

#### 辞書の巨大化
AivisSpeech Engineに巨大な音声合成辞書をユーザー辞書として搭載することで、VoiceSpeechMakerが出るまでは日本一の語彙を持っていた。
以下辞書があるディレクトリ
https://github.com/Aivis-Project/AivisSpeech-Engine/tree/master/resources/dictionaries
辞書はバイナリのみ公開されている

#### 英語カタカナ辞書の追加
AivisSpeechで使われているStyle-Bert-VITS2では、英語とカタカナでの読みがペアになった巨大な辞書で、英語をカタカナに変更することにより、英単語を読ませている
この処理はfork版Style-Bert-VITS2に実装されている。
https://github.com/tsukumijima/Style-Bert-VITS2/blob/fork/style_bert_vits2/nlp/japanese/normalizer.py
英語辞書
https://github.com/tsukumijima/Style-Bert-VITS2/blob/fork/style_bert_vits2/nlp/japanese/katakana_map.py
辞書にない単語は最終的にe2kで推論した読みを採用する


### キャラクターについて

boothで無料配布されているStyle-Bert-VITS2用音声合成モデルの[anneli](https://booth.pm/ja/items/5511064)を使用している。
同キャラクターのAivisSpeechには含まれていないモデル[anneli nsfw](https://booth.pm/ja/items/5511852)も同様にboothで頒布されている
anneli nsfwでは喘ぎ声が生成できる。

### 声優の許諾について
AivisSpeechのデフォルトキャラクターであるanneliだが、無断学習疑惑がある[*1]。


### ライセンスについて

AivisSpeechの依存ライブラリであるStyle-Bert-VITS2はagpl-3ライセンスだが、AivisSpeech-Engine及びAivisSpeechのライセンスはlgpl-3である。
動的リンクはライセンス継承しない、という日本では稀有な見解を持っている可能性がある。

動的リンクはライセンス継承するという判例がどこかで出れば、音声合成apiであるAivis Cloud Apiのソースコードを部分的に開示請求できる可能性がある。

同じくStyle-Bert-VITS2を使用している可能性があるにじボイス（旧DMMボイス）もソースコード開示請求ができるかもしれない。
（先ににじボイス声優無許可使用疑惑から出てくるかもしれない）

ちなみにAivisSpeech製品版ではVoicevox同様逆コンパイルが禁止されている。


### 出典
[*1 にじボイスとAivisSpeechとそっくりな声の声優を探そう！【技術編】](https://zenn.dev/litagin/articles/55db1af37129a8)

### リンク
#### source code (AivisSpeech関連) link

Style-Bert-VITS2 (AivisSpeechで使われているバージョン) 
https://github.com/tsukumijima/Style-Bert-VITS2/tree/fork

AivisSpeech (GUI) 
https://github.com/Aivis-Project/AivisSpeech

AivisSpeech Engine 
https://github.com/Aivis-Project/AivisSpeech-Engine

pyopenjtalk-plus 
https://github.com/tsukumijima/pyopenjtalk-plus


#### AivisSpeech関連サイト

公式サイト
https://aivis-project.com/

X(旧ツイッター)公式アカウント 
https://x.com/aivis_project

公式note
https://note.com/aivis_project

aivm generator 
https://aivm-generator.aivis-project.com/


***other source code link
Style-Bert-VITS2 (original) 
https://github.com/litagin02/Style-Bert-VITS2

e2k
https://github.com/Patchethium/e2k
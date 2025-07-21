### njd_feature 
openjtalk(pyopenjtalk)で使われる型、またその値
中身としては単語ごとのmecabの形態素解析結果とアクセント結合フラグである
  
#### njd_featureと辞書の対応表  
  
フォーマットは  
{csv列番号} {mecab辞書として一般的な名称 英語}|{日本語}　({njd_feature内の名称})  


0 surface|表層系 (string)  
1 left_id｜左文脈id (未使用)  
2 right_id｜右文脈id (未使用)  
3 cost|コスト (未使用)  
4 pos (pos)  
5 pos1 (pos_group1)  
6 pos2 (pos_group2)  
7 pos3 (pos_group3)  
8 活用形 (未使用)   
9 活用形 (未使用)  
10 orig (orig)  
11 read (kana)  
12 pron (pron)  
13 acc/mora (acc),(mora)  
14 acc_con? (?)  
15 tdmelodic_acc (未使用) #tdmelodicでアクセントを推論した場合のtdmelodicの元の出力。  
pyopenjtalk-modの拡張辞書で使われている  
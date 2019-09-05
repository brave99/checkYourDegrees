# checkYourCredits
慶應義塾大学経済学部の進級＆卒業判定システム
プロトタイプ

### 使い方(自分でコピペする方)
keio.jpから出力できる成績表をctrl+A→ctrl+CしてExcel等にコピペしたものを"seiseki.csv"として保存してください。
この時、文字コードをUTF-8にしないと文字化けします。(Excelなら保存時に指定可)<br>
そのcsv及びこの.pyファイルを同じディレクトリに入れて```$ python3 checkCredits.py```でターミナル上に結果が出ます。<br>
外部ライブラリを使用しないため、python3系さえ入っていれば使えます。

### 自動でブラウザを操作する方
1. https://chromedriver.chromium.org/downloads から自身のchromeのバージョンに合ったドライバをダウンロードする。
2. 解凍したchromedriverを同じディレクトリに入れる。
3. config.iniにログインに使う情報を書き込んで上書き保存する。(ここに書かれた情報はログイン時の入力にのみ用いられます)
4. ターミナルを起動し、ディレクトリに入って
```
$ pip3 install selenium
$ python3 getCredits[Mac/Wins].py
```
を実行するとブラウザが動き始め、結果はターミナル上に出力されます。


### 注意
まだプロトタイプなので、誰にでも使いやすいという点はまだ全く満たされていません。
今はとりあえずわかる人にだけテストしてもらえればいいというのが本音です。そういう意味ではオープンβです。<br>
可読性は少しは意識したつもりなので、Python初学者が見ても何やってるかくらいはわかると思います。<br>
何か不具合や疑問点があったらTwitter@azmax007かissueでお願いします。

### 今後の予定
- [x] 卒業判定だけでなく、進級判定も実装する。
- [x] 自動でwebから成績を取ってくる。
- [ ] 履修登録の時点でも使えるようにしたい。(確定した成績でしか判定ができない)
- [ ] プロトタイプはpythonだが、jsかphpあたりで書き直してwebシステム化して本当にコピペするだけで使えるものにして公開したい。
- [ ] 使った感想や要望を集めて、随時TODOを追加する。
- [ ] スクショから読んでほしい(要望出そうだから先に書くけど、多分無理です)

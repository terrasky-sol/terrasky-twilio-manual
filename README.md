# terrasky-twilio-manual
TerraSky-Twilioのマニュアルです。
MkDocsを使用して作成しています。<br>
[マニュアル](https://terrasky-sol.github.io/terrasky-twilio-manual/)
# マニュアルバージョン一覧
Read the Docsを使用してバージョン管理をしています。<br>
[マニュアルバージョン一覧](https://readthedocs.org/projects/terrasky-twilio-manual/)
# MkDocs
Project documentation with Markdown.<br>
View [the MkDocs documentation](https://www.mkdocs.org/).<br>
[公式mkdocsのバージョン一覧](https://readthedocs.org/projects/mkdocs/)
# MkDock使い方日本語の記事（参考）
[MkDocsによるドキュメント作成](https://qiita.com/mebiusbox2/items/a61d42878266af969e3c)<br>
[MkDocs 使ってみた。](https://www.kimoton.com/entry/2017/07/08/121050)<br>
[MkDocs：インストールから github pages へのデプロイまで](https://www.kakistamp.com/entry/2019/08/31/154536)
# マニュアル更新方法
```
#ローカルに落とす
git clone https://github.com/terrasky-sol/terrasky-twilio-manual.git
cd terrasky-twilio-manual

#ビルド
mkdocs build
#ローカルで確認
mkdocs serve

#latestに反映する
git add .
git commit -m "コメント"
git push -u origin master

#バージョンのタグを付けてpushするとそのバージョンのドキュメントが作成される
git tag v1.4.0
git push origin v1.4.0
  
```
# Read the Docs
[公式ドキュメント](https://docs.readthedocs.io/en/stable/)


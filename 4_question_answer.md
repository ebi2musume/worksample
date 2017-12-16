rails g scaffold blog title:string content:text  
というコマンドで生成される以下のファイルを例に説明します。  
  
モデル名　blog 単数形  
ファイル名　blog.rg 単数形  
モデルクラス名　Blog 単数形、頭文字は大文字  
テーブル名　blogs 複数系  
マイグレーションファイル名　xxxxxxxxxxxxxx_create_blogs.rb 複数形  
マイグレーションクラス名　CreateUsers 複数形、頭文字は大文字  
　  
コントローラ名　blogs 複数形  
ファイル名　blogs_controller.rg 複数形  
コントローラクラス名　BlogsController 複数形、頭文字は大文字  

モデルクラスであるBlogは、オブジェクト指向における設計書に当たります。  
Blogという設計書にtitleとcontentという項目を設けています。  
設計書は1つなのでモデルクラス名は単数形で表現されます。  
この設計書をもとに同じ構成を持つインスタンスであるblogを作成していきます。
このblogの情報を保存しているものがblogsテーブルです。
テーブルには複数のblogの情報を保存しているため、テーブル名は複数系で表現されます。
マイグレーションファイルやマイグレーションクラス名は、テーブルを作成するものです。
そのため、テーブル名と同様に複数形で表現されます。
  
Controllerは複数のactionを持つため、複数系で表現されます。
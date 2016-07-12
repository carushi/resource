===========
MySQL
===========


How to start mysql server and input source
------------

brewでmysql.serverを入れてMySQLサーバをローカルで走らせます。

共有する場合にはパスワードなどを真面目にやらないといけないと思いますが、手元でsqlデータセットを見たいときを想定しています。
なので使わないときにはstopしておきます。 ::

	mysql.server start
	mysql -u root
	mysql> SET PASSWORD FOR root@localhost=PASSWORD('hoge')
	mysql> exit
	mysql -u root -h localhost -p #passwordを要求される
	mysql.server stop

Test set
++++++++++

Employdbというやつのfull setを落としてきました。
`https://launchpad.net/test-db/+download <https://launchpad.net/test-db/+download>`_

 ::
 
 	mysql> use db #追加する場合
	mysql> source file
	
このときMysqlのバージョン違いから、storange_engine変数がないというエラーが出たので、 ::

	-- set storage_engine = InnoDB error
	
をコメントアウトしておきました。
新しいバージョンではなくなった変数だそうです。

stopしてもサーバーにデータは残っていますので、データベースを消去するときは ::

	DROP DATABASE IF EXITSTS dbname;

で消せます。
`http://www.liquidweb.com/kb/delete-a-mysql-database-on-linux-via-command-line/ <http://www.liquidweb.com/kb/delete-a-mysql-database-on-linux-via-command-line/>`_


Manage database
--------------

とりあえず表示
++++++++++++

とりあえず表示したいときには ::

	SELECT * FROM tablename WHERE 条件 LIMIT start,end
	
で表示できます。
あとは条件文を設定して絞っていくことになります。

`https://technet.microsoft.com/en-us/library/bb264565(v=sql.90).aspx <https://technet.microsoft.com/en-us/library/bb264565(v=sql.90).aspx>`_

PyMySQLを使う
+++++++++++++

`https://donjajo.com/using-pymysql-as-mysql-driver-for-python3/#.V33kSZN972I <https://donjajo.com/using-pymysql-as-mysql-driver-for-python3/#.V33kSZN972I>`_


GUIでMySQLのデータセットを管理
++++++++++++

macOSではSequel Proが使いやすそうだと思い入れてみました。
tablesの一覧を出してくれて便利。





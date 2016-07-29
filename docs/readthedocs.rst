========================
How to use readthedocs
========================
------------------------------
 New project hosted by github
------------------------------

+++++++++++++++++++++++++++
Creat a new sphinx project
+++++++++++++++++++++++++++

* Reference: `http://rcmdnk.github.io/blog/2016/05/01/computer-brew-file-github/ <http://rcmdnk.github.io/blog/2016/05/01/computer-brew-file-github/>`_
* 以下のコマンドでファイルを初期化する ::

	mkdir test
	cd test
	sphinx-quickstart ## answer or type <enter>

私はMathJaxはenabledにしてみました。
設定は後からconf.pyから変更可能です。

* .gitignore設定 ::

	echo docs/\_build/* > .gitignore

sphinx-quickstartの時点でbuildとsourceを別々にする設定にすると、_buildディレクトリにならないので注意。

* ファイルをgithubにpushしておく ::

	git add -A
	git commit -m'<comment>'
	git push origin <branch>


* localでhtmlを確認 ::

	make html

で_build以下にhtmlファイルができるが、readthedocsではsphinx rds templateが適用されるので見た目違うものになる。

+++++++++++++++++++++++++
Use readthedocs template
+++++++++++++++++++++++++

* テンプレートを使うこともできます。
* `https://github.com/readthedocs/template <https://github.com/readthedocs/template>`_ をフォークするとすぐ試せる



------------------------
Settings of Readthedocs
------------------------

+++++++++++++++++++++++++++
githubのアドレスを指定する
+++++++++++++++++++++++++++

* Admin -> Repository URLでdocumentが入っているレポジトリを指定

++++++++++++++++
buildに失敗する
++++++++++++++++

* Admin -> Advanced Settingsでdocs/conf.pyと指定したら直った
* `http://stackoverflow.com/questions/32729978/read-the-docs-build-failing-without-errors <http://stackoverflow.com/questions/32729978/read-the-docs-build-failing-without-errors>`_


+++++++++++++++
数式サポート
+++++++++++++++

* conf.pyのextensionsに'sphinx.ext.mathbase'を追加

  ::

	.. math::
	    \sum \infty
		
* こうなる→

.. math:: \sum \infty

* `http://shimizukawa-sphinx.readthedocs.io/ja/latest/ext/math.html <http://shimizukawa-sphinx.readthedocs.io/ja/latest/ext/math.html>`_

+++++++++++++++++
Google analytics
+++++++++++++++++

* Admin -> Advanced settingにトラックコードを追加


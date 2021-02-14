Kaggle script build system template
===================================


Init
----

1. get train.csv/test.csv from Kaggle
2. copy them to ``easy_gold/data/input/``
3. edit ``easy_gold/config/default.json`` for data
   a. features
   b. target_name
   c. ID_name
   d. lgbm_params(objective, num_class)


How To Run
----------

```bash
$ cd easy_gold
$ edit run.py for cv setting
$ python run.py
```

How To Add Features
-------------------

1. features/create.pyにclassを追加
2. ``python features/create.py`` 追加した特徴量用のfeatherファイルを生成
3. config/default.jsonのfeaturesに、そのクラス名(小文字スネークケース)を追加し、実行時に追加した特徴量を利用するようにする



How To Create Script For Kaggle Notebook
----------------------------------------

1. ``python build.py`` で ``build/script.py`` が作成される
2. ``build.script.py`` をkaggle notebookにfile uplodaする


License is MIT.

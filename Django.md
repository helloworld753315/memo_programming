# 環境構築

## pyenvのインストール

```sh
$ brew install pyenv
```

## bash_profile(zsh_profile)の編集と適用

```sh
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
```

```sh
$ source ~/.bash_profile
```


## Djangoのインストール

```sh
$ pip install Django==3.1.4
```

## バージョン確認

```sh
python -m django --version
```


# 仮想環境周り

## 仮想環境作成

```sh
$ python -m venv 仮想環境名
```

## Activateにする

```sh
$ source 仮想環境名/bin/activate 
```

## 仮想環境から抜ける

```sh
$ deactivate
```



# サーバー起動

```sh
$ python3 manage.py runserver
```



# プロジェクト作成

```sh
$ django-admin startproject プロジェクト名
```

# ファイル構成

mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
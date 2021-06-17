FROM python:3.7-slim

# 作業ディレクトリを設定
WORKDIR /usr/src/app

# 環境変数を設定
# Pythonがpyc filesとdiscへ書き込むことを防ぐ
ENV PYTHONDONTWRITEBYTECODE 1
# Pythonが標準入出力をバッファリングすることを防ぐ
ENV PYTHONUNBUFFERED 1

RUN apt update \
  && apt install -y apache2-dev \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

# Pipenvをインストール
RUN pip install --upgrade pip \
  && pip install pipenv

# ホストのpipfileをコンテナの作業ディレクトリにコピー
COPY ./Pipfile /usr/src/app/Pipfile

# pipfileからパッケージをインストール
RUN pipenv install --skip-lock --system --dev

# ホストのカレントディレクトリ（現在はappディレクトリ）を作業ディレクトリにコピー
COPY . /usr/src/app/

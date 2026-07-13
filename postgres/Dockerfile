FROM postgres:16-alpine


RUN apk add --no-cache\
    musl-locales\
    musl-locales-lang 

# 改善ポイント③: コンテナ全体に日本語ロケールを適用するための環境変数を明示
ENV LANG=ja_JP.UTF-8 \
    LANGUAGE=ja_JP:ja \
    LC_ALL=ja_JP.UTF-8
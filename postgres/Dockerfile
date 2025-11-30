FROM postgres@sha256:aa7b1ef595e165f0b780162e3a41edd0a7ed3ea672eb8a0f81615ba725e62bc5


RUN apk add --no-cache --update \
    tzdata \
    gettext \
    icu-libs \
    musl-locales \
    && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && echo "Asia/Tokyo" > /etc/timezone


# LANGUAGE ja_JP:ja : 日本語優先
# locales は「言語設定（日本語や英語など）の仕組み」を提供するパッケージです
# -i ja_JP	入力ロケール定義ファイルとして「日本（Japan）」を使う
# -c	すでにある設定に上書きしても続行
# -f UTF-8	文字コードは UTF-8
# -A /usr/share/locale/locale.alias	ロケールの別名リストを参照する
# ja_JP.UTF-8	生成するロケール名（＝完成形の名前）
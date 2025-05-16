FROM python:3.12-slim

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    build-essential \
    default-mysql-client \
    libmariadb-dev \
    pkg-config \
    curl \
    git \
    vim \
    && rm -rf /var/lib/apt/lists/*

# Node.js
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt-get install -y nodejs

# 作業ディレクトリ
WORKDIR /workspace

COPY backend/requirements.txt ./backend/requirements.txt
RUN pip install --upgrade pip && \
    pip install -r ./backend/requirements.txt

COPY . .

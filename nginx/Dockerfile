FROM nginx:latest 

# カスタムのNginx設定ファイルをコンテナ内の指定パスにコピーする
COPY nginx.conf /etc/nginx/nginx.conf  
 # Flaskアプリケーションの設定ファイルをコンテナ内の指定パスにコピーする
COPY flask_app.conf /etc/nginx/sites-available/ 

# ディレクトリを作成（Nginxのサイト有効化設定用）、 シンボリックリンクを作成してFlaskアプリケーションの設定を有効化する
RUN mkdir -p /etc/nginx/sites-enabled/\
    && ln -s /etc/nginx/sites-available/flask_app.conf /etc/nginx/sites-enabled/

# コンテナ起動時にNginxを実行し、デーモンとして動作させる
CMD ["nginx", "-g", "daemon off;"]
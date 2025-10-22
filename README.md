# docker-laravel-home
my-laravel-app/         <-- ホストOS上のプロジェクトルート
├── app/                <-- Laravel本体
├── bootstrap/
├── config/
├── public/
├── storage/
├── vendor/
├── .env                <-- 環境変数（ホスト側、ボリュームマウント用）
├── composer.json
├── package.json
├── docker-compose.yml  <-- 全コンテナ定義（ルートに配置を推奨）
└── docker/             <-- Docker関連ファイルを集約するディレクトリ（名前は自由: `.docker` / `compose` / `infra` でも可）
    ├── nginx/
    │   ├── Dockerfile  <-- Nginxコンテナのビルド用
    │   └── default.conf  <-- Nginxの設定ファイル
    ├── php/
    │   ├── Dockerfile  <-- PHP-FPMコンテナのビルド用
    │   └── php.ini   <-- PHPの設定ファイル
    └── mysql/
        ├── Dockerfile (任意)
        └── my.cnf (任意)
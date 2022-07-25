# new-pr-isucon
初期
{"pass":true,"score":725,"success":639,"fail":1,"messages":["リクエストがタイムアウトしました (POST /register)"]}

変更
make_post関数内の130行目のqueryにおいてcommentsからすべてのデータを取りだしていたが、その後の処理ですべてのデータは用いていないと思ったので、必要なデータのみを取り出すようにして、データを取りだすのにかかる時間を減らした。
前
$query = 'SELECT * FROM `comments` WHERE `post_id` = ? ORDER BY `created_at` DESC';
後
$query = 'SELECT comment, username FROM `comments` WHERE `post_id` = ? ORDER BY `created_at` DESC';
{"pass":true,"score":790,"success":692,"fail":1,"messages":["リクエストがタイムアウトしました (POST /register)"]}       

# new-pr-isucon
# new-pr-isucon

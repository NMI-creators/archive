<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>アーカイブページ</title>
  <style>
    .accordion {
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .accordion summary {
      font-weight: bold;
      padding: 10px;
      cursor: pointer;
      background-color: #f0f0f0;
    }
    .video-link {
      display: flex;
      align-items: center;
      margin: 10px;
      padding: 10px;
      background: #fafafa;
      border: 1px solid #ddd;
      border-radius: 5px;
    }
    .video-link img {
      width: 120px;
      height: auto;
      margin-right: 15px;
    }
    .video-text {
      flex-grow: 1;
    }
    .password-block {
      display: flex;
      align-items: center;
      margin-top: 8px;
    }
    .password {
      background-color: #eee;
      padding: 5px 10px;
      border-radius: 3px;
      margin-right: 8px;
      font-family: monospace;
    }
    .copy-btn {
      padding: 5px 10px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 3px;
      cursor: pointer;
    }
  </style>
  <script>
    function copyPassword(password) {
      navigator.clipboard.writeText(password).then(() => {
        alert("パスワードをコピーしました: " + password);
      });
    }
  </script>
</head>
<body>
  <h1>アーカイブ</h1>

  <!-- ここから物語ブロック -->
  <section>
    <!-- 物語: 凱友伝 -->
    <section>
      <h2>凱友伝</h2>
  <details>
    <summary>第1章</summary>
    <!-- 第1章の内容 -->
    <div class="video-link">
      <a href="動画ページへのリンク" target="_blank">
        <img src="サムネイル画像のURL" alt="サムネイル">
      </a>
      <div class="video-text">
        <p>ここに話数タイトル</p>
        <div class="password-block">
          <span class="password">ここにパスワード</span>
          <button class="copy-btn" onclick="copyPassword('ここにパスワード')">コピー</button>
        </div>
      </div>
    </div>
    <!-- 他の話数も同様に追加 -->
  </details>
</section>

<!-- 物語: エストリア叙事詩 -->
<section>
  <h2>エストリア叙事詩</h2>
  <details>
    <summary>第1章</summary>
    <!-- 第1章の内容 -->
    <div class="video-link">
      <a href="動画ページへのリンク" target="_blank">
        <img src="サムネイル画像のURL" alt="サムネイル">
      </a>
      <div class="video-text">
        <p>ここに話数タイトル</p>
        <div class="password-block">
          <span class="password">ここにパスワード</span>
          <button class="copy-btn" onclick="copyPassword('ここにパスワード')">コピー</button>
        </div>
      </div>
    </div>
    <!-- 他の話数も同様に追加 -->
  </details>
</section>

  </section>
</body>
</html>

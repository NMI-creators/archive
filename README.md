<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>アーカイブページ</title>
  <style>
    .accordion {
      background-color: #f0f0f0;
      cursor: pointer;
      padding: 14px;
      width: 100%;
      text-align: left;
      border: none;
      outline: none;
      transition: 0.4s;
      font-size: 18px;
    }

    .active, .accordion:hover {
      background-color: #ddd;
    }

    .panel {
      padding: 0 18px;
      display: none;
      background-color: white;
      overflow: hidden;
    }

    .video-button {
      display: flex;
      align-items: center;
      margin: 10px 0;
      border: 1px solid #ccc;
      padding: 10px;
      text-decoration: none;
      color: black;
      background-color: #fafafa;
    }

    .video-button img {
      width: 120px;
      height: auto;
      margin-right: 15px;
    }

    .video-info {
      flex-grow: 1;
    }

    .password-box {
      margin-top: 8px;
      background-color: #eee;
      padding: 4px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .copy-btn {
      padding: 3px 8px;
      cursor: pointer;
      background-color: #ccc;
      border: none;
      border-radius: 3px;
    }
  </style>
</head>
<body>

  <h1>ここに物語タイトルを入れる</h1>

  <!-- 各章 -->
  <button class="accordion">ここに章タイトルを入れる</button>
  <div class="panel">

    <!-- 繰り返しパート：動画1つごと -->
    <a class="video-button" href="ここにVimeoのURLを入れる" target="_blank">
      <img src="ここにサムネイル画像のURLを入れる" alt="サムネイル">
      <div class="video-info">
        <div>ここに話数やサブタイトルを入れる</div>
        <div class="password-box">
          <span class="password-text">ここにパスワードを入れる</span>
          <button class="copy-btn" onclick="copyPassword(this)">コピー</button>
        </div>
      </div>
    </a>
    <!-- 繰り返しここまで -->

  </div>

  <!-- アコーディオンのJavaScript -->
  <script>
    const acc = document.getElementsByClassName("accordion");
    for (let i = 0; i < acc.length; i++) {
      acc[i].addEventListener("click", function () {
        this.classList.toggle("active");
        const panel = this.nextElementSibling;
        panel.style.display = panel.style.display === "block" ? "none" : "block";
      });
    }

    function copyPassword(btn) {
      const password = btn.parentElement.querySelector('.password-text').textContent;
      navigator.clipboard.writeText(password).then(() => {
        btn.textContent = "コピー済み";
        setTimeout(() => btn.textContent = "コピー", 2000);
      });
    }
  </script>

</body>
</html>

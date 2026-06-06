<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>名古屋弁</title>
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    background: #000;
    color: #fff;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: "Hiragino Kaku Gothic ProN", "Yu Gothic", sans-serif;
    overflow: hidden;
  }
  .line {
    font-size: 3rem;
    font-weight: bold;
    opacity: 0;
    margin: 1rem 0;
    transition: opacity 1.2s ease;
  }
  .line.show {
    opacity: 1;
  }
  #btn {
    margin-top: 3rem;
    padding: 1rem 3rem;
    font-size: 1.5rem;
    background: #fff;
    color: #000;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    opacity: 0;
    transition: opacity 1.2s ease;
    pointer-events: none;
  }
  #btn.show {
    opacity: 1;
    pointer-events: auto;
  }
</style>
</head>
<body>
  <div class="line" id="line1">名古屋弁のセックス</div>
  <div class="line" id="line2">デラックス。</div>
  <button id="btn">了解。</button>

  <script>
    const line1 = document.getElementById('line1');
    const line2 = document.getElementById('line2');
    const btn   = document.getElementById('btn');

    // 1行目を表示
    setTimeout(() => line1.classList.add('show'), 500);
    // 2行目を表示
    setTimeout(() => line2.classList.add('show'), 2500);
    // ボタンを表示
    setTimeout(() => btn.classList.add('show'), 4500);

    // ボタンを押したら閉じる
    btn.addEventListener('click', () => {
      window.close();
      // window.close() が効かない環境向けのフォールバック
      document.body.innerHTML = '';
      document.body.style.background = '#000';
    });
  </script>
</body>
</html>

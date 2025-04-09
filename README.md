<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Phân Cực | Polarization</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>Phân Cực</h1>
    <p>Blog về đời sống văn học và nghệ thuật</p>
  </header>

  <main>
    <section class="intro">
      <p>Chào mừng bạn đến với <strong>Phân Cực</strong> – nơi ngôn từ gặp gỡ hình ảnh, nơi nghệ thuật được suy tư như một hiện tượng sống động.</p>
    </section>

    <section class="posts">
      <h2>Bài viết gần đây</h2>
      <ul>
        <li><a href="posts/bai-viet-1.html">Tĩnh và Động trong thơ hiện đại</a></li>
        <li><a href="posts/bai-viet-2.html">Biểu tượng và phân mảnh: Nghệ thuật hậu hiện đại</a></li>
      </ul>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Phân Cực</p>
  </footer>
</body>
</html>
🎨 2. style.css – Giao diện
css
Sao chép
Chỉnh sửa
body {
  font-family: Georgia, serif;
  margin: 0;
  background-color: #fefefe;
  color: #222;
}
header {
  background: #222;
  color: white;
  text-align: center;
  padding: 2rem;
}
main {
  max-width: 800px;
  margin: 2rem auto;
  padding: 1rem;
}
.posts ul {
  list-style: none;
  padding: 0;
}
.posts li {
  margin: 1rem 0;
}
.posts a {
  text-decoration: none;
  color: #1a1a1a;
  font-weight: bold;
}
.posts a:hover {
  color: #555;
}
footer {
  text-align: center;
  padding: 1rem;
  background: #eee;
  margin-top: 2rem;
}
✍️ 3. posts/bai-viet-1.html – Một bài viết mẫu có bình luận
html
Sao chép
Chỉnh sửa
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <title>Tĩnh và Động trong thơ hiện đại | Phân Cực</title>
  <link rel="stylesheet" href="../style.css" />
</head>
<body>
  <header>
    <h1>Phân Cực</h1>
    <p>Bài viết: Tĩnh và Động trong thơ hiện đại</p>
  </header>

  <main>
    <article>
      <p>Thơ hiện đại không chỉ là sự phản kháng, mà còn là khoảng lặng... [nội dung mô phỏng]</p>
    </article>

    <section class="comments">
      <h2>Bình luận</h2>
      <textarea id="commentInput" placeholder="Viết bình luận..."></textarea>
      <button onclick="addComment()">Gửi</button>
      <div id="commentList"></div>
    </section>
  </main>

  <footer>
    <p><a href="../index.html">← Về trang chủ</a></p>
  </footer>

  <script src="../script.js"></script>
</body>
</html>
🧠 4. script.js – JavaScript cho bình luận
javascript
Sao chép
Chỉnh sửa
function addComment() {
  const input = document.getElementById("commentInput");
  const list = document.getElementById("commentList");
  const comment = input.value.trim();

  if (comment !== "") {
    const div = document.createElement("div");
    div.className = "comment";
    div.textContent = comment;
    list.appendChild(div);
    input.value = "";
  }
}

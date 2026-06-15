<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>트라페지움 - 천문 관측 커뮤니티</title>
    <style>
        html {
            scroll-behavior: smooth;
        }
        body {
            background-color: #0b132b;
            color: #ffffff;
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #1c2541;
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
        }
        h1 { margin: 0; font-size: 24px; }
        nav a {
            color: #6fffe9;
            text-decoration: none;
            margin-left: 25px;
            font-weight: bold;
        }
        nav a:hover { color: #5bc0be; }
        
        .container {
            padding: 140px 40px 40px 40px;
            max-width: 1100px;
            margin: 0 auto;
        }
        .content-box {
            background-color: #1c2541;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 40px;
            scroll-margin-top: 120px; 
        }
        h2 { color: #5bc0be; margin-top: 0; }
        
        .auth-container {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        .auth-box {
            flex: 1;
            background-color: #0b132b;
            padding: 15px;
            border-radius: 8px;
            border: 1px solid #2a3454;
            min-width: 280px;
        }
        .auth-box h3 { margin-top: 0; color: #6fffe9; font-size: 16px; }
        .auth-form { display: flex; flex-direction: column; gap: 8px; }
        .auth-form input {
            padding: 8px;
            background-color: #1c2541;
            color: white;
            border: 1px solid #5bc0be;
            border-radius: 4px;
        }

        .community-main {
            display: none;
            border-top: 1px solid #2a3454;
            padding-top: 20px;
        }
        
        textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 12px;
            background-color: #0b132b;
            color: white;
            border: 1px solid #5bc0be;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            background-color: #5bc0be;
            color: #0b132b;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
        }
        button:hover { background-color: #6fffe9; }
        .post-list { margin-top: 20px; }
        .post-item { border-bottom: 1px solid #2a3454; padding: 12px 0; }
        .photo-preview { margin-top: 20px; }
        .preview-img { max-width: 300px; margin-top: 15px; border-radius: 5px; display: block; }
    </style>
</head>
<body>

    <header>
        <h1>✨ 트라페지움 (Trapezium)</h1>
        <nav>
            <a href="#info">천문 관측 정보</a>
            <a href="#community">커뮤니티</a>
            <a href="#mypage">내 페이지</a>
        </nav>
    </header>

    <div class="container">
        <div id="info" class="content-box">
            <h2>🔭 오늘의 천문 관측 정보</h2>
            <p>오늘 밤 관측 지수: <b>[매우 좋음]</b></p>
            <p>추천 관측 대상: 토성, 여름철 대삼각형</p>
        </div>

        <div id="community" class="content-box">
            <h2>💬 커뮤니티</h2>
            
            <div class="auth-container" id="authSection">
                <div class="auth-box">
                    <h3>1. 회원가입</h3>
                    <div class="auth-form">
                        <input type="text" id="regId" placeholder="아이디">
                        <input type="password" id="regPw" placeholder="비밀번호">
                        <input type="text" id="regName" placeholder="닉네임">
                        <button onclick="registerUser()">가입하기</button>
                    </div>
                </div>
                <div class="auth-box">
                    <h3>2. 로그인</h3>
                    <div class="auth-form">
                        <input type="text" id="loginId" placeholder="아이디">
                        <input type="password" id="loginPw" placeholder="비밀번호">
                        <button onclick="loginUser()">로그인</button>
                    </div>
                </div>
            </div>

            <div id="welcomeMessage" style="display: none; margin-bottom: 20px; color: #6fffe9; font-weight: bold;"></div>

            <div class="community-main" id="communityMain">
                <p>작성자 닉네임: <b id="userNickname" style="color:#5bc0be;"></b> (로그인된 정보)</p>
                <textarea id="postContent" rows="3" placeholder="이야기를 나누어보세요..."></textarea>
                <button onclick="addPost()">글 쓰기</button>
                <div class="post-list" id="postList">
                    <div class="post-item"><b>스타게이저:</b> 오늘 은하수 촬영 성공했습니다!</div>
                    <div class="post-item"><b>은하수행:</b> 초보자용 망원경 고르는 팁 공유해요.</div>
                </div>
            </div>
        </div>

        <div id="mypage" class="content-box">
            <h2>⭐ 나의 관측 일지 (내 페이지)</h2>
            <p>반가워요, 트라페지움 회원님! 나만의 사진을 보관해 보세요.</p>
            <input type="file" id="imageInput" accept="image/*" onchange="previewImage()">
            <div class="photo-preview" id="photoPreview"></div>
        </div>
    </div>

    <script>
        // 페이지가 열릴 때 컴퓨터(로컬 스토리지)에 저장된 가입 정보를 가져옵니다.
        let savedUser = JSON.parse(localStorage.getItem('trapeziumUser')); 
        let loggedInNickname = ""; 

        // 1. 회원가입 함수 (브라우저 창고에 영구 저장)
        function registerUser() {
            const id = document.getElementById('regId').value;
            const pw = document.getElementById('regPw').value;
            const name = document.getElementById('regName').value;

            if (!id || !pw || !name) {
                alert('회원가입 정보를 모두 입력해 주세요!');
                return;
            }

            savedUser = { id: id, pw: pw, name: name };
            
            // 'trapeziumUser'라는 이름의 칸에 회원 정보를 글자 형태로 바꾼 뒤 저장합니다.
            localStorage.setItem('trapeziumUser', JSON.stringify(savedUser));
            
            alert('회원가입이 완료되었습니다! 이제 로그인을 해주세요.');
            
            document.getElementById('regId').value = '';
            document.getElementById('regPw').value = '';
            document.getElementById('regName').value = '';
        }

        // 2. 로그인 함수
        function loginUser() {
            const id = document.getElementById('loginId').value;
            const pw = document.getElementById('loginPw').value;

            // 새로고침 등으로 변수가 비었다면 저장소에서 다시 가져옵니다.
            if (!savedUser) {
                savedUser = JSON.parse(localStorage.getItem('trapeziumUser'));
            }

            if (!savedUser) {
                alert('가입된 회원 정보가 없습니다. 회원가입을 먼저 해주세요!');
                return;
            }

            if (id === savedUser.id && pw === savedUser.pw) {
                loggedInNickname = savedUser.name;
                
                document.getElementById('authSection').style.display = 'none';
                document.getElementById('welcomeMessage').style.display = 'block';
                document.getElementById('welcomeMessage').innerText = `✨ ${loggedInNickname}님, 환영합니다! 이제 서비스를 이용할 수 있습니다.`;
                
                document.getElementById('userNickname').innerText = loggedInNickname;
                document.getElementById('communityMain').style.display = 'block';
            } else {
                alert('아이디 또는 비밀번호가 틀렸습니다!');
            }
        }

        // 3. 글쓰기 함수
        function addPost() {
            const content = document.getElementById('postContent').value;
            if (!content) return;

            const postList = document.getElementById('postList');
            const newPost = document.createElement('div');
            newPost.className = 'post-item';
            newPost.innerHTML = `<b>${loggedInNickname}:</b> ${content}`;
            
            postList.insertBefore(newPost, postList.firstChild);
            document.getElementById('postContent').value = '';
        }

        // 4. 이미지 미리보기 함수
        function previewImage() {
            const file = document.getElementById('imageInput').files[0];
            const previewContainer = document.getElementById('photoPreview');
            if (!file) return;

            const reader = new FileReader();
            reader.onload = function(e) {
                previewContainer.innerHTML = '';
                const img = document.createElement('img');
                img.src = e.target.result;
                img.className = 'preview-img';
                previewContainer.appendChild(img);
            };
            reader.readAsDataURL(file);
        }
    </script>

</body>
</html>

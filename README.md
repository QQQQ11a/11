<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人主页</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft YaHei", sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
        body {
            background-color: #f7f9fc;
            color: #333;
            line-height: 1.6;
        }
        /* 导航栏 */
        nav {
            width: 100%;
            height: 60px;
            background: #2563eb;
            position: fixed;
            top: 0;
            z-index: 999;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
        }
        .logo {
            color: #fff;
            font-size: 22px;
            font-weight: bold;
        }
        .nav-link a {
            color: #fff;
            text-decoration: none;
            margin: 0 12px;
            font-size: 15px;
            transition: 0.3s;
        }
        .nav-link a:hover {
            color: #bfdbfe;
        }
        /* 通用区块样式 */
        section {
            padding: 80px 5%;
            min-height: 100vh;
        }
        .title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 50px;
            color: #1e40af;
        }
        /* 首页横幅 */
        #home {
            background: linear-gradient(135deg, #2563eb, #60a5fa);
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        #home h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        #home p {
            font-size: 18px;
            max-width: 600px;
            margin-bottom: 30px;
        }
        .btn {
            padding: 12px 30px;
            background: white;
            color: #2563eb;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: 0.3s;
        }
        .btn:hover {
            background: transparent;
            border: 2px solid #fff;
            color: #fff;
        }
        /* 关于我 */
        #about .wrap {
            display: flex;
            gap: 40px;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        .avatar {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: #cbd5e1;
            flex-shrink: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #666;
            font-size: 30px;
        }
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 15px;
        }
        /* 技能板块 */
        #skill {
            background: #ffffff;
        }
        .skill-box {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
        }
        .skill-card {
            padding: 30px;
            background: #f0f7ff;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 2px 8px #e2e8f0;
        }
        .skill-card h4 {
            margin: 10px 0;
            font-size: 20px;
        }
        /* 项目展示 */
        .project-box {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        .project-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 3px 10px #ddd;
        }
        .project-img {
            height: 180px;
            background: #94a3b8;
        }
        .project-info {
            padding: 20px;
        }
        .project-info h4 {
            font-size: 20px;
            margin-bottom: 8px;
        }
        /* 留言表单 */
        #message {
            background: #fff;
        }
        .form-wrap {
            max-width: 600px;
            margin: 0 auto;
        }
        input, textarea {
            width: 100%;
            margin: 8px 0;
            padding: 14px;
            border: 1px solid #ccd6e0;
            border-radius: 8px;
            font-size: 16px;
        }
        textarea {
            height: 140px;
            resize: none;
        }
        .submit-btn {
            width: 100%;
            padding: 14px;
            background: #2563eb;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 17px;
            cursor: pointer;
        }
        .submit-btn:hover {
            background: #1d4ed8;
        }
        /* 页脚 */
        footer {
            background: #1e293b;
            color: #cbd5e1;
            text-align: center;
            padding: 30px;
        }
        footer a {
            color: #60a5fa;
            text-decoration: none;
        }
        /* 移动端适配 */
        @media(max-width:768px){
            .nav-link {
                display: none;
            }
            #home h1 {
                font-size: 32px;
            }
            #about .wrap {
                flex-direction: column;
                text-align: center;
            }
            .avatar {
                width: 200px;
                height: 200px;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav>
        <div class="logo">我的个人站</div>
        <div class="nav-link">
            <a href="#home">首页</a>
            <a href="#about">关于我</a>
            <a href="#skill">技能</a>
            <a href="#project">项目</a>
            <a href="#message">留言</a>
        </div>
    </nav>

    <!-- 首页 -->
    <section id="home">
        <h1>你好，我是一名开发者</h1>
        <p>热爱前端开发、设计与编程，持续学习新技术，专注打造简洁美观的网页作品。</p>
        <a href="#about" class="btn">了解更多</a>
    </section>

    <!-- 关于我 -->
    <section id="about">
        <h2 class="title">关于我</h2>
        <div class="wrap">
            <div class="avatar">头像区域</div>
            <div class="about-text">
                <h3>个人简介</h3>
                <p>大家好！一名热爱互联网技术的开发者，擅长网页开发、页面布局与交互制作。平时喜欢写代码、做设计、分享技术笔记。</p>
                <br>
                <p>性格踏实好学，遇到问题喜欢钻研，业余时间会做开源小项目，持续提升编程能力。</p>
                <br>
                <p>联系方式：邮箱 demo@163.com | 微信：demo666</p>
            </div>
        </div>
    </section>

    <!-- 技能 -->
    <section id="skill">
        <h2 class="title">专业技能</h2>
        <div class="skill-box">
            <div class="skill-card">
                <h4>HTML/CSS</h4>
                <p>页面布局、响应式设计</p>
            </div>
            <div class="skill-card">
                <h4>JavaScript</h4>
                <p>交互逻辑、简单插件开发</p>
            </div>
            <div class="skill-card">
                <h4>Vue</h4>
                <p>前端框架、组件开发</p>
            </div>
            <div class="skill-card">
                <h4>PS设计</h4>
                <p>页面视觉、图片处理</p>
            </div>
        </div>
    </section>

    <!-- 项目作品 -->
    <section id="project">
        <h2 class="title">项目作品</h2>
        <div class="project-box">
            <div class="project-card">
                <div class="project-img"></div>
                <div class="project-info">
                    <h4>企业官网模板</h4>
                    <p>响应式企业静态网站，兼容手机电脑</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-img"></div>
                <div class="project-info">
                    <h4>在线待办清单</h4>
                    <p>JS本地存储待办管理工具</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-img"></div>
                <div class="project-info">
                    <h4>相册展示页面</h4>
                    <p>图片轮播、瀑布流相册布局</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 留言板块 -->
    <section id="message">
        <h2 class="title">给我留言</h2>
        <div class="form-wrap">
            <input type="text" id="name" placeholder="你的姓名">
            <input type="email" id="mail" placeholder="你的邮箱">
            <textarea id="msg" placeholder="写下想说的话..."></textarea>
            <button class="submit-btn" onclick="submitMsg()">提交留言</button>
            <p id="tip" style="text-align:center;margin-top:15px;color:green;"></p>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <p>© 2026 个人个人主页 版权所有</p>
        <p>开源地址：<a href="#">github.com/demo</a></p>
    </footer>

    <!-- JS交互代码 -->
    <script>
        // 留言提交提示
        function submitMsg() {
            let name = document.getElementById("name").value;
            let mail = document.getElementById("mail").value;
            let msg = document.getElementById("msg").value;
            let tip = document.getElementById("tip");
            if(!name || !mail || !msg){
                tip.innerText = "请填写完整信息！";
                tip.style.color = "red";
            }else{
                tip.innerText = "留言提交成功（静态页无后台，仅模拟）";
                tip.style.color = "green";
                // 清空输入框
                document.getElementById("name").value = "";
                document.getElementById("mail").value = "";
                document.getElementById("msg").value = "";
            }
        }
    </script>
</body>
</html>

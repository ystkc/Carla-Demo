---
layout: sidebar
title: 大创项目展示
subtitle: 
---
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>基于的视觉导航系统 - 大创项目展示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Consolas, 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* 标题栏 */
        header {
            background: linear-gradient(135deg, #1a237e, #283593);
            color: white;
            padding: 2.5rem 0;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
            margin-bottom: 30px;
            border-radius: 0 0 15px 15px;
        }

        header h1 {
            font-size: 2.6rem;
            margin-bottom: 0.8rem;
            font-weight: 700;
            letter-spacing: 0.5px;
        }

        header h2 {
            font-size: 1.4rem;
            font-weight: 400;
            opacity: 0.85;
        }

        /* 作者信息 */
        .authors {
            text-align: center;
            margin: 25px 0 35px;
            padding: 20px;
            background-color: #e3f2fd;
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.08);
        }

        .authors h3 {
            color: #1a237e;
            margin-bottom: 15px;
            font-size: 1.6rem;
            position: relative;
            display: inline-block;
            padding-bottom: 8px;
        }

        .authors h3::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 3px;
            background: #5c6bc0;
            bottom: 0;
            left: 20%;
            border-radius: 3px;
        }

        .author-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-top: 25px;
        }

        .author {
            display: flex;
            align-items: center;
            background: white;
            padding: 14px 20px;
            border-radius: 8px;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.05);
            min-width: 220px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .author:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .author-icon {
            width: 48px;
            height: 48px;
            background: linear-gradient(135deg, #7986cb, #3949ab);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.5rem;
            font-weight: bold;
            color: white;
        }

        .author-details {
            text-align: left;
        }

        .author-name {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 3px;
        }

        .author-title {
            color: #555;
            font-size: 0.9rem;
        }

        /* 功能按钮 */
        .actions {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .action-btn {
            background: linear-gradient(135deg, #3949ab, #5c6bc0);
            color: white;
            border: none;
            padding: 14px 30px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 6px 12px rgba(57, 73, 171, 0.35);
        }

        .action-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(57, 73, 171, 0.45);
            background: linear-gradient(135deg, #303f9f, #3949ab);
        }

        .action-btn i {
            font-size: 1.3rem;
        }

        /* 分区标题 */
        .section-title {
            font-size: 2rem;
            color: #1a237e;
            margin: 50px 0 30px;
            padding-bottom: 12px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: #3949ab;
            bottom: 0;
            left: 0;
            border-radius: 2px;
        }

        /* 图片画廊 */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin: 25px 0 35px;
        }

        .gallery-item {
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            background-color: white;
            height: 100%;
        }

        .gallery-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
        }

        .gallery-item img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            display: block;
            border-bottom: 1px solid #f0f0f0;
        }

        .img-caption {
            padding: 18px;
            font-size: 0.95rem;
            color: #444;
        }

        /* 竖屏视频画廊 */
        .video-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 30px;
            margin: 25px 0 40px;
        }

        .video-item {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.4s ease;
        }

        .video-item:hover {
            transform: translateY(-7px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
        }

        /* 竖屏视频容器专用样式 */
        .video-container {
            position: relative;
            width: 100%;
            padding-top: 177.78%; /* 9:16 竖屏比例 */
            background-color: #101010;
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .video-info {
            padding: 18px;
        }

        .video-info h4 {
            margin-bottom: 8px;
            color: #1a237e;
            font-size: 1.3rem;
        }

        .video-info p {
            color: #555;
            font-size: 0.95rem;
        }

        /* 项目介绍 */
        .project-intro {
            background-color: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 6px 18px rgba(0, 0, 0, 0.06);
            margin: 35px 0;
            line-height: 1.8;
        }

        .project-intro p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .highlight {
            background: linear-gradient(to right, #e3f2fd, #bbdefb);
            padding: 3px 8px;
            border-radius: 4px;
            font-weight: 500;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }

        .feature {
            background: #f5f8ff;
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid #5c6bc0;
        }

        .feature h4 {
            color: #3949ab;
            margin-bottom: 10px;
        }

        /* 引用文献 */
        .references {
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 6px 18px rgba(0, 0, 0, 0.06);
            margin: 45px 0;
        }

        .references h3 {
            margin-bottom: 20px;
            color: #1a237e;
            font-size: 1.8rem;
        }

        .reference-list {
            list-style-type: none;
            padding-left: 0;
        }

        .reference-list li {
            margin-bottom: 16px;
            padding: 15px;
            background-color: #f9f9ff;
            border-radius: 6px;
            border-left: 4px solid #5c6bc0;
            transition: all 0.3s ease;
            position: relative;
            padding-left: 60px;
        }

        .reference-list li:hover {
            background-color: #e8eaf6;
        }

        .reference-list li::before {
            content: counter(reference);
            counter-increment: reference;
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            width: 35px;
            height: 35px;
            background: #3949ab;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        /* 页脚 */
        footer {
            text-align: center;
            padding: 35px 0;
            margin-top: 45px;
            color: #4b5563;
            font-size: 0.95rem;
            border-top: 1px solid #e0e0e0;
            background: #f5f7ff;
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .image-gallery, .features, .video-gallery {
                grid-template-columns: 1fr;
            }
            
            header h1 {
                font-size: 2.1rem;
            }
            
            .section-title {
                font-size: 1.7rem;
            }
            
            .author-list {
                flex-direction: column;
                gap: 15px;
            }
            
            .actions {
                gap: 15px;
            }
            
            .action-btn {
                width: 90%;
                justify-content: center;
            }
            
            .reference-list li {
                padding: 15px 15px 15px 50px;
            }
        }
    </style>
</head>
<!-- fontawesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w==" crossorigin="anonymous" />
<body>
    <!-- 标题栏 -->
    <header>
        <div class="container">
            <h1>视觉导航系统 - 大创项目展示</h1>
            <h2>项目介绍...</h2>
        </div>
    </header>

    <div class="container">
        <!-- 作者信息 -->
        <section class="authors">
            <h3>研究团队</h3>
            <div class="author-list">
                <div class="author">
                    <div class="author-icon">Z</div>
                    <span>张明 (项目负责人)</span>
                </div>
                <div class="author">
                    <div class="author-icon">L</div>
                    <span>李华 (首席研究员)</span>
                </div>
                <div class="author">
                    <div class="author-icon">W</div>
                    <span>王林 (算法工程师)</span>
                </div>
                <div class="author">
                    <div class="author-icon">Z</div>
                    <span>赵雪 (数据科学家)</span>
                </div>
            </div>
        </section>

        <!-- 功能按钮 -->
        <div class="actions">
            <button id="videoBtn" class="action-btn">
                <i class="fas fa-video"></i> 展示视频
            </button>
            <button id="githubBtn" class="action-btn">
                <i class="fab fa-github"></i> GitHub项目
            </button>
            <button id="dataBtn" class="action-btn">
                <i class="fas fa-database"></i> 实验数据集
            </button>
        </div>

        <!-- 图片画廊 -->
        <h3 class="section-title">项目演示</h3>
        <div class="image-gallery">
            <div class="gallery-item">
                <img src="{{ site.baseurl }}/static/img/1.jpg" alt="图片1">
                <div class="img-caption">说明1</div>
            </div>
            <div class="gallery-item">
                <img src="{{ site.baseurl }}/static/img/2.jpg" alt="图片2">
                <div class="img-caption">说明2</div>
            </div>
            <div class="gallery-item">
                <img src="{{ site.baseurl }}/static/img/3.jpg" alt="图片3">
                <div class="img-caption">说明3</div>
            </div>
            <div class="gallery-item">
                <img src="{{ site.baseurl }}/static/img/4.jpg" alt="图片4">
                <div class="img-caption">说明4</div>
            </div>
        </div>

        <!-- 项目介绍 -->
        <h3 class="section-title">项目介绍</h3>
        <section class="project-intro">
            <p>本项目旨在开发一种基于<span class="highlight">技术</span>的视觉导航技术</p>
            
            <p>该系统的主要技术优势包括：</p>
            <ul>
                <li>创新的双路径特征提取机制</li>
                <li>自适应空间注意力模型</li>
                <li>三维可视化结果展示界面</li>
            </ul>
            
            <p>经过严格实地验证，该系统在多个领域的应用效果优于传统方法。</p>
        </section>

        <!-- 视频画廊 -->
        <h3 class="section-title">视频展示</h3>
        <div class="video-gallery">
            <div class="video-item">
                <div class="video-container">
                    <iframe src="{{ site.baseurl }}/static/video/1.mp4" allowfullscreen></iframe>
                </div>
                <div class="video-info">
                    <h4>系统核心功能演示</h4>
                    <p>展示系统的主要功能模块和用户界面操作流程</p>
                </div>
            </div>
            <div class="video-item">
                <div class="video-container">
                    <iframe src="{{ site.baseurl }}/static/video/2.mp4" allowfullscreen></iframe>
                </div>
                <div class="video-info">
                    <h4>演示</h4>
                    <p>说明</p>
                </div>
            </div>
        </div>

        <!-- 引用文献 -->
        <section class="references">
            <h3>参考文献</h3>
            <ol class="reference-list">
                <li>参考文献1</li>
            </ol>
        </section>
    </div>

    <footer>
        <div class="container">
            <p>研究组 © 2023 | 研究中心</p>
            <p>联系方式： | 地址：</p>
        </div>
    </footer>

    <script>
        // 功能按钮交互
        document.getElementById('videoBtn').addEventListener('click', function() {
            alert('即将跳转到项目展示视频页面...');
            // 实际应用中在此处添加视频页面跳转代码
            // window.location.href = 'https://example.com/project-video';
        });

        document.getElementById('githubBtn').addEventListener('click', function() {
            alert('即将跳转到GitHub项目仓库...');
            // 实际应用中在此处添加GitHub页面跳转代码
            // window.location.href = 'https://github.com/example/project';
        });

        document.getElementById('dataBtn').addEventListener('click', function() {
            alert('即将跳转到实验数据下载页面...');
            // 实际应用中在此处添加数据页面跳转代码
            // window.location.href = 'https://example.com/project-data';
        });

        // 图片画廊交互
        document.querySelectorAll('.gallery-item').forEach(item => {
            item.addEventListener('click', function() {
                // 在新标签页打开图片
                window.open(item.querySelector('img').src);
            });
        });
    </script>
</body>
</html>
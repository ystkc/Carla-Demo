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
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
            background: linear-gradient(135deg, #1a56db, #0e2a7c);
            color: white;
            padding: 2rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
            border-radius: 0 0 15px 15px;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        header h2 {
            font-size: 1.3rem;
            font-weight: 400;
            opacity: 0.9;
        }

        /* 作者信息 */
        .authors {
            text-align: center;
            margin: 25px 0;
            padding: 15px;
            background-color: #ebf4ff;
            border-radius: 10px;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
        }

        .authors h3 {
            color: #1a56db;
            margin-bottom: 10px;
        }

        .author-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .author {
            display: flex;
            align-items: center;
        }

        .author-icon {
            width: 40px;
            height: 40px;
            background-color: #93c5fd;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 10px;
            font-weight: bold;
            color: #1e3a8a;
        }

        /* 功能按钮 */
        .actions {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .action-btn {
            background: linear-gradient(135deg, #1d4ed8, #3b82f6);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 8px rgba(59, 130, 246, 0.3);
        }

        .action-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(59, 130, 246, 0.4);
        }

        .action-btn i {
            font-size: 1.2rem;
        }

        /* 分区标题 */
        .section-title {
            font-size: 1.8rem;
            color: #1e3a8a;
            margin: 35px 0 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #93c5fd;
            display: inline-block;
        }

        /* 图片画廊 */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .gallery-item {
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            background-color: white;
        }

        .gallery-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }

        .gallery-item img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            display: block;
        }

        .img-caption {
            padding: 15px;
            font-size: 0.9rem;
            color: #4b5563;
        }

        /* 视频画廊 */
        .video-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 25px;
            margin: 20px 0;
        }

        .video-container {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding-top: 56.25%; /* 16:9 Aspect Ratio */
            background-color: #1a202c;
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
            padding: 15px;
            background-color: white;
            border-radius: 0 0 10px 10px;
        }

        .video-info h4 {
            margin-bottom: 5px;
            color: #1e40af;
        }

        /* 项目介绍 */
        .project-intro {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin: 25px 0;
            line-height: 1.8;
        }

        .project-intro p {
            margin-bottom: 20px;
        }

        .highlight {
            background-color: #dbeafe;
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: 500;
        }

        /* 引用文献 */
        .references {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin: 25px 0;
        }

        .references h3 {
            margin-bottom: 15px;
            color: #1e40af;
        }

        .reference-list {
            list-style-type: none;
        }

        .reference-list li {
            margin-bottom: 12px;
            padding-left: 20px;
            position: relative;
        }

        .reference-list li::before {
            content: "•";
            color: #3b82f6;
            font-size: 1.5rem;
            position: absolute;
            left: 0;
            top: -4px;
        }

        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 30px;
            color: #4b5563;
            font-size: 0.9rem;
            border-top: 1px solid #e5e7eb;
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .image-gallery {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            
            header h1 {
                font-size: 2rem;
            }
            
            .actions {
                flex-direction: column;
                align-items: center;
            }
            
            .action-btn {
                width: 80%;
                justify-content: center;
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
                alert('点击查看大图: ' + this.querySelector('.img-caption').textContent);
            });
        });
    </script>
</body>
</html>
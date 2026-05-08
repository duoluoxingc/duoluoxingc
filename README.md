<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>堕落星辰 · duoluoxingc</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #e0e0e0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* 星尘粒子背景效果 */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .card {
            position: relative;
            z-index: 1;
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 24px;
            padding: 50px 40px;
            max-width: 520px;
            width: 100%;
            text-align: center;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6), 
                        0 0 80px rgba(102, 126, 234, 0.1);
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #1a1a3e, #2d1b4e, #1a1a3e);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 24px;
            font-size: 52px;
            color: #c4b5fd;
            box-shadow: 0 8px 30px rgba(139, 92, 246, 0.3),
                        inset 0 0 30px rgba(139, 92, 246, 0.1);
            border: 2px solid rgba(139, 92, 246, 0.3);
        }

        h1 {
            font-size: 30px;
            font-weight: 700;
            background: linear-gradient(135deg, #c4b5fd, #e9d5ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 6px;
            letter-spacing: 2px;
        }

        .username {
            font-size: 13px;
            color: #7c7caa;
            margin-bottom: 28px;
            letter-spacing: 3px;
            font-family: 'Courier New', monospace;
        }

        .divider {
            width: 60px;
            height: 2px;
            background: linear-gradient(90deg, transparent, #8b5cf6, #a78bfa, #8b5cf6, transparent);
            margin: 0 auto 28px;
            border-radius: 2px;
        }

        .bio {
            font-size: 15px;
            line-height: 1.8;
            color: #b8b8d8;
            margin-bottom: 36px;
            padding: 0 10px;
        }

        .links {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .link-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 14px 24px;
            border-radius: 14px;
            text-decoration: none;
            font-size: 15px;
            font-weight: 600;
            letter-spacing: 2px;
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }

        .link-btn.primary {
            background: linear-gradient(135deg, #6d28d9, #7c3aed);
            color: #fff;
            box-shadow: 0 6px 20px rgba(139, 92, 246, 0.3);
            border: 1px solid rgba(139, 92, 246, 0.4);
        }

        .link-btn.primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 30px rgba(139, 92, 246, 0.5);
        }

        .link-btn.outline {
            background: transparent;
            border: 1px solid rgba(139, 92, 246, 0.25);
            color: #c8c8e8;
        }

        .link-btn.outline:hover {
            background: rgba(139, 92, 246, 0.08);
            border-color: rgba(139, 92, 246, 0.5);
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(139, 92, 246, 0.15);
        }

        .social {
            display: flex;
            justify-content: center;
            gap: 18px;
            margin-top: 32px;
        }

        .social-icon {
            width: 44px;
            height: 44px;
            border-radius: 50%;
            background: rgba(139, 92, 246, 0.08);
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 20px;
            color: #a78bfa;
            transition: all 0.3s ease;
            border: 1px solid rgba(139, 92, 246, 0.15);
        }

        .social-icon:hover {
            background: rgba(139, 92, 246, 0.2);
            color: #ddd6fe;
            transform: translateY(-4px);
            box-shadow: 0 8px 20px rgba(139, 92, 246, 0.3);
        }

        .footer {
            margin-top: 32px;
            font-size: 11px;
            color: #555;
            letter-spacing: 2px;
            font-family: 'Courier New', monospace;
        }

        @media (max-width: 480px) {
            .card {
                padding: 36px 24px;
            }
            h1 {
                font-size: 26px;
            }
            .avatar {
                width: 100px;
                height: 100px;
                font-size: 44px;
            }
        }
    </style>
</head>
<body>
    <div class="card">
        <!-- 头像：一颗坠落的星星 ✦ 或者你可以换成 "辰" 字 -->
        <div class="avatar">✦</div>

        <!-- 名字 & ID -->
        <h1>堕落星辰</h1>
        <p class="username">@duoluoxingc</p>

        <div class="divider"></div>

        <!-- 简介 -->
        <p class="bio">
            坠落，是为了更耀眼地升起。<br>
            代码 · 思考 · 创造 · 永恒
        </p>

        <!-- 主要链接按钮 -->
        <div class="links">
            <a href="https://github.com/duoluoxingc" class="link-btn primary" target="_blank">
                ⭐ GitHub 主页
            </a>
            <a href="#" class="link-btn outline">
                📁 项目作品
            </a>
            <a href="#" class="link-btn outline">
                ✉️ 与我联系
            </a>
        </div>

        <!-- 社交链接 -->
        <div class="social">
            <a href="https://github.com/duoluoxingc" class="social-icon" title="GitHub" target="_blank">🐙</a>
            <a href="mailto:your-email@example.com" class="social-icon" title="邮箱">📧</a>
            <a href="#" class="social-icon" title="更多">🌐</a>
        </div>

        <p class="footer">✦ 堕落星辰 · duoluoxingc · Powered by GitHub Pages ✦</p>
    </div>
</body>
</html>

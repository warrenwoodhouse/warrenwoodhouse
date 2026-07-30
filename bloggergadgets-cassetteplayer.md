Code for implementing your very own 80s inspired Cassette Player for your own HTML website.
Replace “PLAYLIST_ID” with your own playlist id from your own YouTube channel or any YouTube channel you like.

# code
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>70s & 80s Mixtape Player</title>
    <style>
        body {
            background-color: #2c2c2c;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            font-family: 'Courier New', Courier, monospace;
            color: #fff;
        }

        /* Cassette Outer Shell */
        .cassette {
            width: 400px;
            height: 250px;
            background-color: #dcdcdc;
            border-radius: 15px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.5), 5px 5px 15px rgba(0,0,0,0.6);
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            box-sizing: border-box;
        }

        /* Screws */
        .screw {
            width: 12px;
            height: 12px;
            background-color: #999;
            border-radius: 50%;
            position: absolute;
            box-shadow: inset 1px 1px 3px rgba(0,0,0,0.5);
        }
        .screw::after {
            content: "";
            position: absolute;
            width: 8px;
            height: 2px;
            background-color: #555;
            top: 5px;
            left: 2px;
            transform: rotate(45deg);
        }
        .tl { top: 10px; left: 10px; }
        .tr { top: 10px; right: 10px; }
        .bl { bottom: 10px; left: 10px; }
        .br { bottom: 10px; right: 10px; }

        /* Sticker Label */
        .label {
            width: 85%;
            height: 130px;
            background: linear-gradient(180deg, #ff9a44 0%, #fc6076 100%);
            border-radius: 8px;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: inset 0 0 5px rgba(0,0,0,0.2);
        }

        .title {
            background: #fff;
            color: #000;
            width: 90%;
            text-align: center;
            margin-top: 10px;
            padding: 5px;
            font-weight: bold;
            font-size: 1.2rem;
            border-radius: 3px;
        }

        /* Center Window */
        .window {
            width: 220px;
            height: 60px;
            background-color: #1a1a1a;
            margin-top: 15px;
            border-radius: 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.8);
            position: relative;
        }

        /* Tape inside window */
        .tape-bridge {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 120px;
            height: 20px;
            background-color: #333;
            z-index: 0;
        }

        /* Reels */
        .reel {
            width: 50px;
            height: 50px;
            background-color: #fff;
            border-radius: 50%;
            z-index: 1;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .reel-center {
            width: 15px;
            height: 15px;
            background-color: #1a1a1a;
            border-radius: 50%;
        }

        .spoke {
            position: absolute;
            width: 4px;
            height: 100%;
            background-color: #ccc;
        }
        .spoke:nth-child(2) { transform: rotate(60deg); }
        .spoke:nth-child(3) { transform: rotate(120deg); }

        /* Animation for spinning tape */
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .playing .reel {
            animation: spin 3s linear infinite;
        }

        /* Bottom trapezoid area */
        .bottom-section {
            width: 280px;
            height: 45px;
            background-color: #c0c0c0;
            position: absolute;
            bottom: 0;
            clip-path: polygon(10% 0, 90% 0, 100% 100%, 0% 100%);
            box-shadow: inset 0 10px 10px rgba(0,0,0,0.1);
        }

        /* Controls */
        .controls {
            margin-top: 30px;
            display: flex;
            gap: 15px;
        }

        button {
            background-color: #444;
            color: #fff;
            border: 2px solid #222;
            padding: 10px 20px;
            font-family: inherit;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 5px;
            box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
            transition: background 0.2s, transform 0.1s;
        }

        button:active {
            transform: translateY(2px);
            box-shadow: 0 0 2px rgba(0,0,0,0.5);
        }

        button:hover {
            background-color: #555;
        }

        /* Hidden YouTube iframe wrapper */
        #youtube-container {
            position: absolute;
            top: -9999px;
            left: -9999px;
        }
        
        .status {
            margin-top: 15px;
            font-size: 0.9rem;
            color: #aaa;
        }
    </style>
</head>
<body>

    <div class="cassette" id="cassette">
        <div class="screw tl"></div>
        <div class="screw tr"></div>
        <div class="screw bl"></div>
        <div class="screw br"></div>
        
        <div class="label">
            <div class="title">Awesome Mix: 70s & 80s</div>
            <div class="window">
                <div class="tape-bridge"></div>
                <div class="reel">
                    <div class="spoke"></div>
                    <div class="spoke"></div>
                    <div class="spoke"></div>
                    <div class="reel-center"></div>
                </div>
                <div class="reel">
                    <div class="spoke"></div>
                    <div class="spoke"></div>
                    <div class="spoke"></div>
                    <div class="reel-center"></div>
                </div>
            </div>
        </div>
        <div class="bottom-section"></div>
    </div>

    <div class="controls">
        <button id="btn-play">▶ Play</button>
        <button id="btn-pause">⏸ Pause</button>
        <button id="btn-next">⏭ Next Track</button>
    </div>
    
    <div class="status" id="status-text">Loading tape...</div>

    <!-- Hidden container for YouTube Player -->
    <div id="youtube-container">
        <div id="player"></div>
    </div>

    <script>
        let player;
        const cassette = document.getElementById('cassette');
        const statusText = document.getElementById('status-text');

        // Load the YouTube IFrame Player API code asynchronously.
        const tag = document.createElement('script');
        tag.src = "https://www.youtube.com/iframe_api";
        const firstScriptTag = document.getElementsByTagName('script')[0];
        firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

        // This function creates an <iframe> (and YouTube player) after the API code downloads.
        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '10',
                width: '10',
                // This is a massive public playlist of 70s and 80s hit songs
                playerVars: {
                    'listType': 'playlist',
                    'list': 'PLAYLIST_ID', 
                    'controls': 0,
                    'disablekb': 1,
                    'fs': 0,
                    'autoplay': 0
                },
                events: {
                    'onReady': onPlayerReady,
                    'onStateChange': onPlayerStateChange,
                    'onError': onPlayerError
                }
            });
        }

        function onPlayerReady(event) {
            statusText.innerText = "Tape Ready. Press Play.";
            
            // Wire up the HTML buttons to the YouTube Player
            document.getElementById('btn-play').addEventListener('click', () => {
                player.playVideo();
            });

            document.getElementById('btn-pause').addEventListener('click', () => {
                player.pauseVideo();
            });

            document.getElementById('btn-next').addEventListener('click', () => {
                player.nextVideo();
            });
        }

        // When the player's state changes (e.g., playing, paused)
        function onPlayerStateChange(event) {
            if (event.data === YT.PlayerState.PLAYING) {
                cassette.classList.add('playing');
                statusText.innerText = "Playing Audio...";
            } else if (event.data === YT.PlayerState.PAUSED) {
                cassette.classList.remove('playing');
                statusText.innerText = "Paused.";
            } else if (event.data === YT.PlayerState.ENDED) {
                cassette.classList.remove('playing');
                player.nextVideo();
            } else if (event.data === YT.PlayerState.BUFFERING) {
                cassette.classList.remove('playing');
                statusText.innerText = "Fast Forwarding / Buffering...";
            }
        }

        function onPlayerError(event) {
            // Skips unplayable/deleted videos in the playlist automatically
            player.nextVideo();
        }
    </script>
</body>
</html>
```

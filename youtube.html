<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTubeClonebyJunryPacot</title>
    <link rel="stylesheet" href="style.css">
</head>
<style>
    /* General styles */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: Arial, sans-serif;
        background-color: #000000;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        flex-direction: column;
    }

    .container {
        width: 100%;
        max-width: 800px;
        margin: 20px;
    }

    h1 {
        text-align: center;
        margin-bottom: 20px;
    }

    .search-box {
        display: flex;
        justify-content: center;
        margin-bottom: 20px;
    }

    #search-input {
        width: 70%;
        padding: 10px;
        font-size: 16px;
        border: 2px solid #ccc;
        border-radius: 5px;
    }

    #search-button {
        padding: 10px;
        font-size: 16px;
        background-color: #ff0000;
        border: none;
        color: white;
        cursor: pointer;
        border-radius: 5px;
        margin-left: 10px;
    }

    #search-button:hover {
        background-color: #ff787d;
    }

    #videos-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }

    .video-item {
        width: 320px;
        margin: 15px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        background-color: #ffffff;
        position: relative;
        overflow: hidden;
    }

    .video-item iframe {
        width: 100%;
        height: 200px;
        border: none;
    }

    .loading-indicator {
        position: absolute;
        top: 30%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 16px;
        color: #ffffff;
    }

    .download-button {
        padding: 8px;
        background-color: #28a745;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        margin-top: 10px;
        display: block;
        text-align: center;
        text-decoration: none;
    }

    .download-button:hover {
        background-color: #218838;
    }

    .timer {
        font-size: 14px;
        color: #333;
        margin-top: 5px;
    }

    .volume-control {
        margin-top: 10px;
    }

    .volume-container {
        margin-top: 10px;
        display: flex;
        flex-direction: column;
        align-items: start;
    }

    .volume-label {
        font-size: 14px;
        color: #333;
        margin-bottom: 5px;
    }

    #developer-credit {
        text-align: center;
        margin-bottom: 20px;
        font-size: 18px;
        color: #ffffff;
    }

    #developer-credit a {
        color: #0000ff;
        text-decoration: none;
    }

    #developer-credit a:hover {
        color: #0000ff;
        text-decoration: underline;
    }

    #loading-spinner {
        display: none;
        border: 8px solid #f3f3f3;
        border-radius: 50%;
        border-top: 8px solid #3498db;
        width: 60px;
        height: 60px;
        animation: spin 1s linear infinite;
        margin: 20px auto;
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>
<body>
    <div class="container">
        <div id="developer-credit">
            <p>Developed by <a href="https://www.facebook.com/profile.php?id=100075262125552" target="_blank">Junry Pacot</a></p>
        </div>
        
        <h1>YouTube Video Search</h1>
        
        <div class="search-box">
            <input type="text" id="search-input" placeholder="Search for videos...">
            <button id="search-button">Search</button>
        </div>
        
        <div id="loading-spinner"></div>
        <div id="videos-container"></div>
    </div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        const searchButton = document.getElementById('search-button');
        const searchInput = document.getElementById('search-input');
        const videosContainer = document.getElementById('videos-container');
        const loadingSpinner = document.getElementById('loading-spinner');
        let players = [];

        // Replace with your YouTube Data API key
        const API_KEY = 'AIzaSyALgVmFt23O1NR0cfOUJZsBF8IlVBCWUn8';
        const API_URL = 'https://www.googleapis.com/youtube/v3/search';

        searchButton.addEventListener('click', async () => {
            const query = searchInput.value;

            if (query) {
                videosContainer.innerHTML = ''; // Clear previous results
                loadingSpinner.style.display = 'block'; // Show loading spinner

                const url = `${API_URL}?part=snippet&q=${encodeURIComponent(query)}&type=video&key=${API_KEY}&maxResults=10`;

                try {
                    const response = await fetch(url);
                    const data = await response.json();

                    loadingSpinner.style.display = 'none'; // Hide loading spinner

                    if (data.items) {
                        displayVideos(data.items);
                    } else {
                        videosContainer.innerHTML = '<p>No videos found</p>';
                    }
                } catch (error) {
                    console.error('Error fetching videos:', error);
                    loadingSpinner.style.display = 'none'; // Hide loading spinner
                    videosContainer.innerHTML = '<p>Something went wrong, please try again later.</p>';
                }
            }
        });

        function displayVideos(videos) {
            videosContainer.innerHTML = ''; // Clear previous results
            players = [];

            videos.forEach(video => {
                const videoElement = document.createElement('div');videoElement.classList.add('video-item');

                videoElement.innerHTML = `
                    <div class="loading-indicator">Loading video...</div>
                    <div id="player-${video.id.videoId}"></div>
                    <h3>${video.snippet.title}</h3>
                    <p>${video.snippet.description}</p>
                    <a href="https://en.savefrom.net/1-youtube-video-downloader-3/?url=https://www.youtube.com/watch?v=${video.id.videoId}" class="download-button" target="_blank">Download</a>
                    <div class="timer" id="timer-${video.id.videoId}">Time: 0:00 | Remaining: 0:00</div>
                    
                    <!-- Volume control with label -->
                    <div class="volume-container">
                        <label for="volume-${video.id.videoId}" class="volume-label">Volume:</label>
                        <input type="range" id="volume-${video.id.videoId}" class="volume-control" min="0" max="100" value="100">
                    </div>
                `;

                videosContainer.appendChild(videoElement);

                // Initialize YouTube player
                const player = new YT.Player(`player-${video.id.videoId}`, {
                    videoId: video.id.videoId,
                    events: {
                        'onReady': onPlayerReady,
                        'onStateChange': onPlayerStateChange
                    }
                });

                players.push({ player, videoId: video.id.videoId });
            });
        }

        // Update timer and volume while video is playing
        function onPlayerStateChange(event) {
            const player = event.target;
            const videoId = player.getIframe().id.split('-')[1];
            const timerElement = document.getElementById(`timer-${videoId}`);
            const volumeControl = document.getElementById(`volume-${videoId}`);

            if (event.data === YT.PlayerState.PLAYING) {
                const interval = setInterval(() => {
                    const currentTime = player.getCurrentTime();
                    const duration = player.getDuration();
                    const remainingTime = duration - currentTime;

                    const minutes = Math.floor(currentTime / 60);
                    const seconds = Math.floor(currentTime % 60);

                    const remMinutes = Math.floor(remainingTime / 60);
                    const remSeconds = Math.floor(remainingTime % 60);

                    timerElement.textContent = `Time: ${minutes}:${seconds < 10 ? '0' + seconds : seconds} | Remaining: ${remMinutes}:${remSeconds < 10 ? '0' + remSeconds : remSeconds}`;

                    if (event.data !== YT.PlayerState.PLAYING) {
                        clearInterval(interval);
                    }
                }, 1000);

                // Update volume control
                volumeControl.addEventListener('input', (e) => {
                    player.setVolume(e.target.value);
                });
            }
        }

        function onPlayerReady(event) {
            const iframe = event.target.getIframe();
            iframe.style.display = 'block';
            iframe.previousElementSibling.style.display = 'none'; // Remove loading message
        }
    </script>
</body>
</html>

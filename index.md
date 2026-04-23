cutlab
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CutLab — Video Editor</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Outfit:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg: #0a0a0c; --bg2: #111115; --bg3: #18181f; --bg4: #1f1f28;
            --border: #2a2a35; --border2: #35354a;
            --accent: #e8ff47; --accent2: #7c6af5; --text: #f0f0f8;
            --text2: #9090aa; --text3: #55556a;
            --clip-video: #2d4a7a; --header-h: 52px; --timeline-h: 220px;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { width: 100%; height: 100vh; overflow: hidden; background: var(--bg); color: var(--text); font-family: 'Outfit', sans-serif; font-size: 13px; }

        /* HEADER */
        #header {
            height: var(--header-h); background: var(--bg2); border-bottom: 1px solid var(--border);
            display: flex; align-items: center; padding: 0 16px; justify-content: space-between;
        }
        .logo { font-family: 'Bebas Neue', sans-serif; font-size: 24px; letter-spacing: 3px; color: var(--accent); }
        .logo span { color: var(--text2); }

        /* MAIN LAYOUT */
        #main { display: flex; height: calc(100vh - var(--header-h) - var(--timeline-h)); }

        #left-panel { width: 240px; background: var(--bg2); border-right: 1px solid var(--border); display: flex; flex-direction: column; }
        .panel-tabs { display: flex; border-bottom: 1px solid var(--border); overflow-x: auto; }
        .panel-tab { padding: 12px; cursor: pointer; font-size: 10px; font-weight: 700; color: var(--text3); text-transform: uppercase; }
        .panel-tab.active { color: var(--accent); border-bottom: 2px solid var(--accent); }
        .panel-content { flex: 1; overflow-y: auto; padding: 15px; }

        /* PREVIEW AREA */
        #center { flex: 1; display: flex; flex-direction: column; background: #000; position: relative; }
        #preview-wrap { flex: 1; display: flex; align-items: center; justify-content: center; overflow: hidden; }
        #main-video { max-width: 90%; max-height: 90%; box-shadow: 0 0 50px rgba(0,0,0,0.5); border-radius: 4px; }

        /* TIMELINE */
        #timeline { height: var(--timeline-h); background: var(--bg2); border-top: 1px solid var(--border); position: relative; }
        #playhead { position: absolute; top: 0; left: 100px; width: 2px; height: 100%; background: var(--accent); z-index: 10; pointer-events: none; }
        
        .track-row { height: 45px; border-bottom: 1px solid var(--border); position: relative; width: 2000px; }
        .clip { position: absolute; height: 35px; top: 5px; background: var(--clip-video); border-radius: 4px; border: 1px solid rgba(255,255,255,0.1); padding: 5px; font-size: 10px; }

        /* UTILS */
        .hidden { display: none !important; }
        #file-input { display: none; }
        .upload-zone { border: 2px dashed var(--border2); padding: 20px; text-align: center; border-radius: 8px; cursor: pointer; }
    </style>
</head>
<body>

<div id="header">
    <div class="logo">CUT<span>LAB</span></div>
    <div class="header-right">
        <button style="background:var(--accent); border:none; padding:8px 15px; border-radius:5px; font-weight:bold; cursor:pointer;">Export</button>
    </div>
</div>

<div id="main">
    <div id="left-panel">
        <div class="panel-tabs">
            <div class="panel-tab active" onclick="switchTab('media')">Media</div>
            <div class="panel-tab" onclick="switchTab('fx')">FX</div>
        </div>
        <div id="media-content" class="panel-content">
            <div class="upload-zone" onclick="document.getElementById('file-input').click()">
                <p>+ Upload Video</p>
            </div>
            <input type="file" id="file-input" accept="video/*">
            <div id="media-list" style="margin-top:15px;"></div>
        </div>
        <div id="fx-content" class="panel-content hidden">
            <p style="color:var(--text3)">No effects applied</p>
        </div>
    </div>

    <div id="center">
        <div id="preview-wrap">
            <video id="main-video" controls></video>
            <div id="drop-hint">No video selected</div>
        </div>
    </div>
</div>

<div id="timeline">
    <div id="playhead"></div>
    <div style="overflow-x: auto; height: 100%;">
        <div class="track-row" id="video-track">
            <!-- Clips will appear here -->
        </div>
        <div class="track-row"></div>
    </div>
</div>

<script>
    const fileInput = document.getElementById('file-input');
    const mainVideo = document.getElementById('main-video');
    const mediaList = document.getElementById('media-list');
    const dropHint = document.getElementById('drop-hint');
    const videoTrack = document.getElementById('video-track');

    // 1. Tab Switching Logic
    function switchTab(tab) {
        document.querySelectorAll('.panel-tab').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.panel-content').forEach(c => c.classList.add('hidden'));
        
        event.currentTarget.classList.add('active');
        document.getElementById(`${tab}-content`).classList.remove('hidden');
    }

    // 2. File Upload & Preview Logic
    fileInput.addEventListener('change', function(e) {
        const file = e.target.files[0];
        if (file) {
            const url = URL.createObjectURL(file);
            
            // Show in preview
            mainVideo.src = url;
            mainVideo.style.display = 'block';
            dropHint.classList.add('hidden');

            // Add to Sidebar
            const thumb = document.createElement('div');
            thumb.style.cssText = "background:var(--bg4); padding:10px; border-radius:5px; margin-bottom:5px; cursor:pointer;";
            thumb.innerText = file.name;
            thumb.onclick = () => { mainVideo.src = url; };
            mediaList.appendChild(thumb);

            // Add to Timeline (Simulated)
            const clip = document.createElement('div');
            clip.className = 'clip';
            clip.style.width = "150px";
            clip.style.left = "50px";
            clip.innerText = file.name;
            videoTrack.appendChild(clip);
        }
    });

    // 3. Playhead Movement (Mockup)
    mainVideo.addEventListener('timeupdate', () => {
        const progress = (mainVideo.currentTime / mainVideo.duration) * 500; // scaling factor
        document.getElementById('playhead').style.left = (100 + progress) + 'px';
    });
</script>

</body>
</html>

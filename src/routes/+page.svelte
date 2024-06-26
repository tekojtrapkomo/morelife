<script>
    let videoUrl = "/more.mp4"; // Replace this with the path to your video file
    let video;
    let isPlaying = false;
  
    function togglePlayPause() {
      if (video.paused) {
        video.play();
        isPlaying = true;
      } else {
        video.pause();
        isPlaying = false;
      }
    }

  </script>
  
  <div class="text">
    <h1>MORE</h1>
    <h1>LIFE</h1>
  </div>
  <div class="text2">
    <h1>MORE</h1>
    <h1>TO</h1>
    <h1>LIVE</h1>
  </div>
  <div class="wrapper">
    <div class="video-container">
      <video bind:this={video} src={videoUrl} loop >
        <track kind="captions">
        Your browser does not support the video tag.
      </video>
      <div class="controls">
        <button on:click={togglePlayPause}>{isPlaying ? 'Pause' : 'Play'}</button>
      </div>
    </div>
  </div>
  
  <style>
    .wrapper {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      width: 100%;
      background-color: #151515;
      flex-direction: column;
      overflow: hidden;
      font-family: 'default';
    }
  
    .video-container {
      width: 70%;
      max-width: 1200px;
      aspect-ratio: 16 / 9;
      position: relative;
    }
  
    video {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border: none;
    }
  
    .controls {
      display: none;
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 10px;
      padding: 10px;
      border-radius: 5px;
    }
  
    .video-container:hover .controls {
      display: flex;
    }
  
    .controls button {
      background: rgba(255, 255, 255, 0.8);
      border: none;
      color: black;
      padding: 10px;
      cursor: pointer;
      font-size: 14px;
      border-radius: 5px;
    }
  
    .controls button:hover {
      background: rgba(255, 255, 255, 1);
    }
  
    .text h1 {
      color: white;
      font-size: 11px;
      text-align: center;
      font-family: 'default';
    }
  
    .text {
      width: 100%;
      display: flex;
      justify-content: space-between;
      padding: 0.5em 1em;
      background-color: #151515;
    }
  
    .text2 {
      width: 100%;
      display: flex;
      position: absolute;
      bottom: 0;
      justify-content: space-between;
      background-color: #151515;
    }
  
    .text2 h1 {
      color: white;
      font-size: 11px;
      text-align: center;
      font-family: 'default';
      padding: 0.5em 1em;
    }
  </style>
  
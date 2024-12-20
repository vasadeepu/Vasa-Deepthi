# Vasa-Deepthi
// Original code with hardcoded video ID
// var videoId = 'M7lc1UVf-VE';

// Modified code to use a variable for the video ID
var videoId = 'M7lc1UVf-VE';  // Replace this ID with the desired video ID

// Example of dynamically setting the video ID
function loadYouTubeVideo(videoId) {
    var player;
    function onYouTubeIframeAPIReady() {
        player = new YT.Player('player', {
            height: '390',
            width: '640',
            videoId: videoId,
            events: {
                'onReady': onPlayerReady,
                'onStateChange': onPlayerStateChange
            }
        });
    }

    function onPlayerReady(event) {
        event.target.playVideo();
    }

    function onPlayerStateChange(event) {
        if (event.data == YT.PlayerState.PLAYING) {
            // Video is playing
        }
    }
}

// Call the function with the desired video ID
loadYouTubeVideo(videoId);

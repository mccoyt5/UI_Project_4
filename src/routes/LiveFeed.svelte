<script>
    import { Link } from "svelte-routing";

    // Simulate a transcription that would appear when talking with someone on the live feed
    let transcription = "";
    let words = ["Here", " is", " an", " example", " of", " a", " transcription."];
    let i = 0;
    let stopTranscription = false;
    $: {
        if (stopTranscription == false) {
            setTimeout(function(){
                transcription += words[i];
                i++;
                if (i >= 7) {
                    stopTranscription = true;
                }
            }, 200);
        }
    }
</script>
  
<Link to="/">
    <button class="return">Go Back</button>
</Link>

<h2 id="viewerName"> Talking to: John Doe</h2>
<!-- Image source: https://www.britannica.com/biography/John-Krasinski  -->
<img id="currentViewer" src="./American-actor-John-Krasinski-2020.webp" alt="John">
<p id="transcription">Transcription: {transcription}</p>

<style>
    .return {
        float: left;
        margin-top: 15px;
        margin-left: 20px;
    }

    #viewerName {
        float: right;
        margin-top: 12.5px;
        margin-right: 20px;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        font-size: x-large;
    }

    #currentViewer {
        height: 500px;
        width: 370px;
        margin-top: 15px;
    }

    #transcription {
        float: left;
        margin-top: -5px;
        margin-left: 20px;
    }
</style>

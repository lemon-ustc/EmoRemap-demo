<script>
function pauseOthers(ele) {
    $("audio").not(ele).each(function (index, audio) {audio.pause();});
}
</script>

<style>
.main-content table {
    display: inline-table;
}
table {
    table-layout:fixed;
    width: 100%;
    overflow: hidden;
}
#player{
    width: 100%;
}
#players{
    width: 300px;
}
.center-text {
            text-align: center;
        }	
</style>

# EmoRemap

## Abstract
<p align="justify">
Abstract: Although current Text-To-Speech (TTS) models are able to generate high-quality speech samples, emotion intensity controllable TTS remains a difficult challenge. Most existing TTS models achieve emotion intensity control by extracting intensity information from reference speeches. Unfortunately, limited by the lack of modeling for intra-class emotion intensity and the model's information decoupling capability, the generated speech cannot achieve fine-grained emotion intensity control and suffers from information leakage issues. In this paper, we propose an emotion transfer TTS model, which defines a remapping method to model intra-class relative intensity information, combined with mutual information (MI) to decouple speaker and emotion information, and synthesizes expressive speeches with clearly perceivable intensity. Experiments show that our model achieves fine-grained emotion control while preserving speaker information.
</p>

## Overview
<p align="justify">

</p>

![Model Architecture ](assets/frame.png)
<p align="center">Figure.1 The Architecture of EmoRemap</p>
<p>&nbsp;</p> 

## Samples
Audio samples are taken from the ESD dataset.

### Intensity Controllability

<div class="center-text"><p> Reference Audio - Happy </p></div>
<div class="center-text"><audio controls id="players" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </div>
<table>
	<CAPTION>Text: Traditional Voice Conversion!</CAPTION>
    <tr>
        <th> Intensity </th>
        <th> 0.2 </th>
        <th> 0.4 </th>
        <th> 0.6 </th>
	<th> 0.8 </th>
    </tr>
<tr>
        <th> FEC </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
</tr>
    <tr>
        <th> Intensity </th>
        <th> -0.4 </th>
        <th> -0.2 </th>
        <th> 0.2 </th>
	<th> 0.4 </th>
    </tr>
<tr>
        <th> Ours </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p374_070.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/M2Mp374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
</tr>	
</table>

<p>&nbsp;</p> 

<div class="center-text"><p> Reference Audio - Sad </p></div>
<div class="center-text"><audio controls id="players" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </div>
<table>
	<CAPTION>Text: Traditional Voice Conversion!</CAPTION>
    <tr>
        <th> Intensity </th>
        <th> 0.2 </th>
        <th> 0.4 </th>
        <th> 0.6 </th>
	<th> 0.8 </th>
    </tr>
<tr>
        <th> FEC </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
</tr>
    <tr>
        <th> Intensity </th>
        <th> -0.4 </th>
        <th> -0.2 </th>
        <th> 0.2 </th>
	<th> 0.4 </th>
    </tr>
<tr>
        <th> Ours </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p374_070.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/M2Mp374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
</tr>	
</table>

<p>&nbsp;</p> 

<div class="center-text"><p> Reference Audio - Angry </p></div>
<div class="center-text"><audio controls id="players" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </div>
<table>
	<CAPTION>Text: Traditional Voice Conversion!</CAPTION>
    <tr>
        <th> Intensity </th>
        <th> 0.2 </th>
        <th> 0.4 </th>
        <th> 0.6 </th>
	<th> 0.8 </th>
    </tr>
<tr>
        <th> FEC </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
</tr>
    <tr>
        <th> Intensity </th>
        <th> -0.4 </th>
        <th> -0.2 </th>
        <th> 0.2 </th>
	<th> 0.4 </th>
    </tr>
<tr>
        <th> Ours </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p374_070.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/M2Mp374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
</tr>	
</table>

<p>&nbsp;</p> 

<div class="center-text"><p> Reference Audio - Surprise </p></div>
<div class="center-text"><audio controls id="players" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </div>
<table>
	<CAPTION>Text: Traditional Voice Conversion!</CAPTION>
    <tr>
        <th> Intensity </th>
        <th> 0.2 </th>
        <th> 0.4 </th>
        <th> 0.6 </th>
	<th> 0.8 </th>
    </tr>
<tr>
        <th> FEC </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> </th>
</tr>
    <tr>
        <th> Intensity </th>
        <th> -0.4 </th>
        <th> -0.2 </th>
        <th> 0.2 </th>
	<th> 0.4 </th>
    </tr>
<tr>
        <th> Ours </th>
	<th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p374_070.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/ADAINVC/s2s/p374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
        <th> <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/M2Mp374_070_p286_028.mp3" type="audio/mpeg"></audio> </th>
</tr>	
</table>

<p>&nbsp;</p> 



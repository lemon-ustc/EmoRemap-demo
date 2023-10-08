# EmoRemap

## Abstract
<!-- <p align="justify"> -->
Abstract: Although current Text-To-Speech (TTS) models are able to generate high-quality speech samples, emotion intensity controllable TTS remains a difficult challenge. Most existing TTS models achieve emotion intensity control by extracting intensity information from reference speeches. Unfortunately, limited by the lack of modeling for intra-class emotion intensity and the model's information decoupling capability, the generated speech cannot achieve fine-grained emotion intensity control and suffers from information leakage issues. In this paper, we propose an emotion transfer TTS model, which defines a remapping method to model intra-class relative intensity information, combined with mutual information (MI) to decouple speaker and emotion information, and synthesizes expressive speeches with clearly perceivable intensity. Experiments show that our model achieves fine-grained emotion control while preserving speaker information.
</p>

## Overview
<p align="justify">

</p>

![Model Architecture ](assets/frame.png)
<p align="center">Figure.1 The Architecture of EmoRemap</p>
<p>&nbsp;</p> 
<script>
function pauseOthers(ele) {
    $("audio").not(ele).each(function (index, audio) {audio.pause();});
}
</script>

<style>
.main-content table {
    display: inline-table;
    margin: 0 auto;
}
table {
    table-layout:fixed;
    width: 100%;
    overflow: hidden;
}
#nums{
        text-align:center; 
        width: 50px;
}
#player{
    width: 220px;
}
#players{
    width: 300px;
} 
</style>

<style>
.custom-span {
        width: px;
        }
.center-text {
        text-align: center;
        }
</style>

## Samples
Audio samples are taken from the ESD dataset.

### Samples Comparison 

<div class="center-text"><p>Text</p></div>
<div class="center-text"><p>I Love You</p></div>
<div class="center-text">Reference Audio</div>
<div class="center-text"><audio controls id="players" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p228_154.mp3" type="audio/mpeg"></audio></div>

<table>
	<tr>
        <th style="text-align:center"> </th>
        <th style="text-align:center"> FEC </th>
        <th style="text-align:center">  </th>
	<th style="text-align:center"> Ours </th>
	</tr>
	<tr>
	<th> 0.2 </th>
	<th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio>
        </th>
        <th> -0.4 </th> 
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
	</tr>
	<tr>
        <th> 0.4 </th> 
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio>
        </th>
        <th> -0.2 </th> 
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
	</tr>
</table>


<p>&nbsp;</p> 

### Emotion Intensity Controllability

<table>
	<tr>
        <th style="text-align:center"> </th>
        <th style="text-align:center"> 0.2/-0.4 </th>
        <th style="text-align:center"> 0.4/-0.2 </th>
        <th style="text-align:center"> 0.6/0.2 </th>
	<th style="text-align:center"> 0.8/0.4 </th>
	</tr>
	<tr>
        <th> FEC </th> 
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio>
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
	</tr>
	<tr>
        <th> Ours </th> 
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/s2s_raw/p233_025.mp3" type="audio/mpeg"></audio>
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
        <th>
        <audio controls id="player" onplay="pauseOthers(this);"><source src="assets/MAINVC/s2s/F2Fp228_154_p233_025.mp3" type="audio/mpeg"></audio> 
        </th>
	</tr>
</table>






<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta name="description" content="">
    <meta name="author" content="OlaWod">

    <title>FreeVC Demo Page</title>

    <!-- Bootstrap core CSS -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.1/css/bootstrap.min.css" rel="stylesheet">

    <!-- Custom fonts for this template -->
    <link href="vendor/fontawesome-free/css/all.min.css" rel="stylesheet" type="text/css">
    <link href='https://fonts.googleapis.com/css?family=Lora:400,700,400italic,700italic' rel='stylesheet' type='text/css'>
    <link href='https://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,800italic,400,300,600,700,800' rel='stylesheet' type='text/css'>

    <!-- Custom styles for this template -->
    <link href="css/clean-blog.css" rel="stylesheet">
	
	<link rel="stylesheet" href="./css/fontawesome.all.min.css">
	
	<script defer src="./js/fontawesome.all.min.js"></script>
	<!-- Bootstrap core JavaScript -->
	<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
	<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>

	<!-- Custom scripts for this template -->
	<script src="js/clean-blog.js"></script>
	<script src="js/interp.js"></script>

</head>

<body id="page-top">

	<nav class="navbar navbar-expand-lg fixed-top" id="mainNav">
		<div class="container">
			<a class="navbar-brand js-scroll-trigger" href="#page-top">FreeVC</a>
			<button class="navbar-toggler navbar-toggler-right font-weight-bold text-white rounded" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">Menu <i class="fas fa-bars"></i></button>
            <div class="collapse navbar-collapse" id="navbarResponsive">
				<ul class="navbar-nav ml-auto">
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#abstract">Abstract</a>
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#sr">Spectrogram-Resize</a></li>
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#s2s">Seen-to-Seen</a></li>
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#u2s">Unseen-to-Seen</a></li>
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#u2u">Unseen-to-Unseen</a></li>
					<li class="nav-item mx-0 mx-lg-1"><a class="nav-link py-3 px-0 px-lg-3 rounded js-scroll-trigger" href="#exp">Others</a></li>
				</ul>
			</div>
		</div>
	</nav>

    <!-- Page Header -->
    <header class="masthead" style="background-image: url('img/home-bg.jpg')">
        <div class="container" style="padding-bottom:10px">
            <div class="row">
                <div class="col-lg-10 col-md-10 mx-auto">
                    <div class="site-heading">
                        <h1>FreeVC Demo</h1>
                        <span class="subheading">
                            FREEVC: TOWARDS HIGH-QUALITY TEXT-FREE ONE-SHOT VOICE CONVERSION
                        </span>
                    </div>
                </div>
            </div>
			
            <div class="text-center">
              <!-- PDF Link. -->
              <span class="link-block">
                <a href="https://arxiv.org/abs/2210.15418" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fas fa-file-pdf fa-inverse"></i>
                  </span>
                  <span>Paper</span>
                </a>
              </span>
              <!-- Code Link. -->
              <span class="link-block">
                <a href="https://github.com/OlaWod/FreeVC" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fab fa-github fa-inverse"></i>
                  </span>
                  <span>Code</span>
                  </a>
              </span>
            </div>
			
        </div>
    </header>

    <!-- Main Content -->
    <div class="container">
        <div class="row">
            <div class="col-lg-14 col-md-12 mx-auto">
                <div class="post-preview" id="abstract">
                    <h2 class="post-title">
                        Abstract
                    </h2>
                    <p>
                        Voice conversion (VC) can be achieved by first extracting source content information and target speaker information, and then reconstructing waveform with these information. However, current approaches normally either extract dirty content information with speaker information leaked in, or demand a large amount of annotated data for training. Besides, the quality of reconstructed waveform can be degraded by the mismatch between conversion model and vocoder. In this paper, we adopt the end-to-end framework of VITS for high-quality waveform reconstruction, and propose strategies for clean content information extraction without text annotation. We disentangle content information by imposing an information bottleneck to WavLM features, and propose the spectrogram-resize based data augmentation to improve the purity of extracted content information. Experimental results show that the proposed method outperforms the latest VC models trained with annotated data and has greater robustness.
						
					</p>
                </div>
				
				<div class="post-preview" id="sr">
                    <h2 class="post-title">
                        Spectrogram-Resize
                    </h2>
                    
					<div class="hero-body">
						<div class="content has-text-justified">
						  <p>
							Use the sliders below to perform vertical or horizontal spectrogram-resize operation.
						  </p>
						</div>
						<div class="columns is-vcentered interpolation-panel">
						  <div class="column">
						    <div id="interpolation-audio-wrapper">
							  Loading audio...
							</div>
							<div id="interpolation-image-wrapper">
							  Loading image...
							</div>
							<div id="vertical-slider-wrapper">
								<span>&nbsp &nbsp veritical: </span>
								<input class="slider is-fullwidth is-large is-info"
								   id="vertical-slider"
								   step="2" min="68" max="92" value="80" type="range">
								<span id="vertical-rate">1</span>
							</div>
							<div id="horizontal-slider-wrapper">
							<span>horizontal: </span>
							<input class="slider is-fullwidth is-large is-info"
								   id="horizontal-slider"
								   step="10" min="96" max="346" value="176" type="range">
							<span id="horizontal-rate">1</span>
							</div>
						  </div>
						</div>
						<br/>
						<!--/ Interpolating. -->
					</div>
					
                </div>			
				
                <div class="post-preview">
                    <h2 class="post-title">
                        One-shot Voice Conversion
                    </h2>
                    <h3 class="post-meta" id="s2s">
                        Seen-to-Seen
                    </h3>
                    <table class="table">
                        <thead>
                            <tr>
                                <th scope="col">Source</th>
                                <th scope="col">Target</th>
                                <th scope="col">Conversion</th>
                            </tr>
                        </thead>
                        <tbody>
                            
                            <tr>
                                <td>F_p335_302
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p335_302.wav">
                                    </audio>
                                </td>
                                <td>F_p253_219
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p253_219.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\s2s\F_p335_302-F_p253_219_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\s2s\F_p335_302-F_p253_219.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\s2s\F_p335_302-F_p253_219.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\s2s\F_p335_302-F_p253_219.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\s2s\F_p335_302-F_p253_219.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\s2s\F_p335_302-F_p253_219.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>F_p362_103
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p362_103.wav">
                                    </audio>
                                </td>
                                <td>M_p237_001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p237_001.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\s2s\F_p362_103-M_p237_001_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\s2s\F_p362_103-M_p237_001.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\s2s\F_p362_103-M_p237_001.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\s2s\F_p362_103-M_p237_001.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\s2s\F_p362_103-M_p237_001.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\s2s\F_p362_103-M_p237_001.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_p237_001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p237_001.wav">
                                    </audio>
                                </td>
                                <td>F_p335_302
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p335_302.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\s2s\M_p237_001-F_p335_302_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\s2s\M_p237_001-F_p335_302.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\s2s\M_p237_001-F_p335_302.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\s2s\M_p237_001-F_p335_302.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\s2s\M_p237_001-F_p335_302.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\s2s\M_p237_001-F_p335_302.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_p272_219
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p272_219.wav">
                                    </audio>
                                </td>
                                <td>M_p259_464
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p259_464.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\s2s\M_p272_219-M_p259_464_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\s2s\M_p272_219-M_p259_464.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\s2s\M_p272_219-M_p259_464.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\s2s\M_p272_219-M_p259_464.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\s2s\M_p272_219-M_p259_464.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\s2s\M_p272_219-M_p259_464.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                        </tbody>
                    </table>
					<hr>
					<h3 class="post-meta" id="u2s">
                        Unseen-to-Seen
                    </h3>
                    <table class="table">
                        <thead>
                            <tr>
                                <th scope="col">Source</th>
                                <th scope="col">Target</th>
                                <th scope="col">Conversion</th>
                            </tr>
                        </thead>
                        <tbody>
                            
                            <tr>
                                <td>F_5142_36377_000004_000012
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_5142_36377_000004_000012.wav">
                                    </audio>
                                </td>
                                <td>F_p253_219
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p253_219.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2s\F_5142_36377_000004_000012-F_p253_219_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2s\F_5142_36377_000004_000012-F_p253_219.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2s\F_5142_36377_000004_000012-F_p253_219.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2s\F_5142_36377_000004_000012-F_p253_219.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2s\F_5142_36377_000004_000012-F_p253_219.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2s\F_5142_36377_000004_000012-F_p253_219.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>F_8463_287645_000023_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_8463_287645_000023_000001.wav">
                                    </audio>
                                </td>
                                <td>M_p237_001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p237_001.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2s\F_8463_287645_000023_000001-M_p237_001_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2s\F_8463_287645_000023_000001-M_p237_001.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2s\F_8463_287645_000023_000001-M_p237_001.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2s\F_8463_287645_000023_000001-M_p237_001.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2s\F_8463_287645_000023_000001-M_p237_001.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2s\F_8463_287645_000023_000001-M_p237_001.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_1320_122617_000013_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_1320_122617_000013_000001.wav">
                                    </audio>
                                </td>
                                <td>F_p335_302
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_p335_302.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2s\M_1320_122617_000013_000001-F_p335_302_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2s\M_1320_122617_000013_000001-F_p335_302.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2s\M_1320_122617_000013_000001-F_p335_302.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2s\M_1320_122617_000013_000001-F_p335_302.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2s\M_1320_122617_000013_000001-F_p335_302.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2s\M_1320_122617_000013_000001-F_p335_302.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_5105_28233_000016_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_5105_28233_000016_000001.wav">
                                    </audio>
                                </td>
                                <td>M_p259_464
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_p259_464.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2s\M_5105_28233_000016_000001-M_p259_464_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2s\M_5105_28233_000016_000001-M_p259_464.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2s\M_5105_28233_000016_000001-M_p259_464.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2s\M_5105_28233_000016_000001-M_p259_464.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2s\M_5105_28233_000016_000001-M_p259_464.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2s\M_5105_28233_000016_000001-M_p259_464.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                        </tbody>
                    </table>
					<hr>
					<h3 class="post-meta" id="u2u">
                        Unseen-to-Unseen
                    </h3>
                    <table class="table">
                        <thead>
                            <tr>
                                <th scope="col">Source</th>
                                <th scope="col">Target</th>
                                <th scope="col">Conversion</th>
                            </tr>
                        </thead>
                        <tbody>
                            
                            <tr>
                                <td>F_3575_170457_000032_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_3575_170457_000032_000001.wav">
                                    </audio>
                                </td>
                                <td>M_5105_28233_000016_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_5105_28233_000016_000001.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2u\F_3575_170457_000032_000001-M_5105_28233_000016_000001.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>F_8463_287645_000023_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_8463_287645_000023_000001.wav">
                                    </audio>
                                </td>
                                <td>F_3575_170457_000032_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_3575_170457_000032_000001.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2u\F_8463_287645_000023_000001-F_3575_170457_000032_000001.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_5105_28233_000016_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_5105_28233_000016_000001.wav">
                                    </audio>
                                </td>
                                <td>M_1320_122617_000013_000001
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_1320_122617_000013_000001.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2u\M_5105_28233_000016_000001-M_1320_122617_000013_000001.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                            <tr>
                                <td>M_908_31957_000018_000000
                                    <audio controls preload="none">
                                        <source src="data\wavs\M_908_31957_000018_000000.wav">
                                    </audio>
                                </td>
                                <td>F_5142_36377_000004_000012
                                    <audio controls preload="none">
                                        <source src="data\wavs\F_5142_36377_000004_000012.wav">
                                    </audio>
                                </td>
                                <td>
									VQMIVC
                                    <audio controls preload="none">
                                        <source src="data/vqmivc\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012_gen.wav">
                                    </audio> 
									BNE-PPG-VC
                                    <audio controls preload="none">
                                        <source src="data/bne-ppg-vc\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012.wav">
                                    </audio>
									YourTTS
                                    <audio controls preload="none">
                                        <source src="data/yourtts\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012.wav">
                                    </audio>
                                </td>
                                <td>
								    FreeVC
                                    <audio controls preload="none">
                                        <source src="data/freevc\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012.wav">
                                    </audio> 
									FreeVC (w/o SR)
                                    <audio controls preload="none">
                                        <source src="data/freevc-sr\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012.wav">
                                    </audio>
									FreeVC-s
                                    <audio controls preload="none">
                                        <source src="data/freevc-spk\u2u\M_908_31957_000018_000000-F_5142_36377_000004_000012.wav">
                                    </audio>
                                </td>
                            </tr>
                            
                        </tbody>
                    </table>
                </div>
                <hr>
				
				<div class="post-preview" id="exp">
                    <h2 class="post-title">
                        Additional Experiments
                    </h2>
                    <p>
						We also conduct objective experiments to other models that are not listed in the paper. 
						We randomly select 400 utterances (200 from VCTK, 200 from LibriTTS) as source speech, 
						and 12 speakers (6 seen, 6 unseen) as target speaker. 
						The results are shown below.
					</p>
					<img src="data/exp/model.png">
					<img src="data/exp/exp1.png">
					<img src="data/exp/exp2.png">
                </div>
				<hr>
				
            </div>
        </div>
		</div>


</body>

</html>
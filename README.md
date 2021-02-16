
<!DOCTYPE html>
<html>
<head>
<base href="//static.diep.io/">
<link rel="icon" type="image/png" href="/favicon-32x32.png" sizes="32x32">
<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96">
<link rel="icon" type="image/png" href="/favicon-16x16.png" sizes="16x16">
<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">
<title>diep.io</title>
<meta name="description" content="Survive and shoot at others while trying to keep your own tank alive!">
<style>

body {
	background-color: #000000;
}

html, body, #canvas {
	border: 0;
	margin: 0;
	padding: 0;
	overflow: hidden;
}

#loading {
	color: #FFFFFF;
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	font-size: 48pt;
	font-family: sans-serif;
	font-weight: bold;
	cursor: default;
}

#canvas {
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	width: 100%;
	height: 100%;
	cursor: default;
}

#textInputContainer {
	display: none;
	position: absolute;
}

#textInput {
	background-color: transparent;
	font-family: 'Ubuntu';
	padding: 0;
	border: 0;
	outline: none;
}

#a {
	position: absolute;
    bottom: 0px;
    left: 50%;
    pointer-events: none;
}

.aa {
	background-color: transparent;
	
	margin: 24px auto;
	border-radius: 5px;
	overflow: hidden;
}

.aa-tall {
	width: 300px;
	height: 250px;
}

.aa-wide {
	width: 728px;
	height: 90px;
}

</style>
</head>
<body>
<script>
	(function(m,n,c,l,i,p,t){m[c]=m[c]||function(){2===arguments.length&&
		(m[c].q=m[c].q||[]).push(arguments)};m.MCApolloPageView=m[c];
		p=n.createElement('script');t=n.getElementsByTagName('script')[0];
		p.async=0;m.mc_ap_pv_c_n=i;p.src=l;t.parentNode.insertBefore(p,t)})
	(window,document,'Apollo','//apollo.miniclip.com/v1/js','diep.io');
</script>
<script async src="https://js-sec.indexww.com/ht/htw-mc-diep.js"></script>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<script src="https://c.n.m28.io/sdk.js"></script>
<script type='text/javascript'>
	var googletag = googletag || {};
	googletag.cmd = googletag.cmd || [];
	(function() {
		var gads = document.createElement('script');
		gads.async = true;
		gads.type = 'text/javascript';
		gads.src = 'https://www.googletagservices.com/tag/js/gpt.js';
		var node = document.getElementsByTagName('script')[0];
		node.parentNode.insertBefore(gads, node);
	})();
</script>
<link href='https://fonts.googleapis.com/css?family=Ubuntu:700' rel='stylesheet' type='text/css'>
<span id="loading">Loading...</span>
<canvas id="canvas" width="800" height="800"></canvas>
<div id="a">
<div style="position: relative; left: -50%; pointer-events: auto;">
<div id="a1" class="aa"><div id="ac1"></div></div>
<div id="a2" class="aa" style="display:none"><div id="ac2"></div></div>
<div id="a3" class="aa" style="display:none"><div id="ac3"></div></div>
</div>
</div>
<div id="empty-container"></div>
<div style="position: absolute; width: 640px; height: 360px; top: 50%; left: 50%; margin-left: -320px; margin-top: -180px; display: none;">
<div id="player" style="width: 100%; height: 100%;"></div>
</div>
<script>
	var initialAds = [];
	var mainAds = [];
	var statsAds = [];
	
	googletag.cmd.push(function() {
		var aa = document.querySelectorAll(".aa");
		
		if(window.innerHeight < 710){
			for(var i = 0; i < aa.length; ++i) aa[i].classList.add("aa-wide");
			
			initialAds.push(googletag.defineSlot('/116850162/Diep.io_728x90_initial', [728, 90], 'ac1').addService(googletag.pubads()));
			mainAds.push(googletag.defineSlot('/116850162/Diep.io_728x90_main', [728, 90], 'ac2').addService(googletag.pubads()));
			statsAds.push(googletag.defineSlot('/116850162/Diep.io_728x90_stats', [728, 90], 'ac3').addService(googletag.pubads()));
		}else{
			for(var i = 0; i < aa.length; ++i) aa[i].classList.add("aa-tall");
			
			initialAds.push(googletag.defineSlot('/116850162/Diep.io_300x250_initial', [300, 250], 'ac1').addService(googletag.pubads()));
			mainAds.push(googletag.defineSlot('/116850162/Diep.io_300x250_main', [300, 250], 'ac2').addService(googletag.pubads()));
			statsAds.push(googletag.defineSlot('/116850162/Diep.io_300x250_stats', [300, 250], 'ac3').addService(googletag.pubads()));
		}
		
		
		googletag.pubads().enableSingleRequest();
		googletag.pubads().disableInitialLoad();
		googletag.enableServices();
		
		googletag.display('ac1');
		googletag.display('ac2');
		googletag.display('ac3');
		googletag.pubads().refresh(initialAds);
		
		window["ads2"] = true;
	});
</script>
<div style="font-family:'Ubuntu'">&nbsp;</div>
<div id="textInputContainer"><input id="textInput" /></div>

<script async src="https://www.googletagmanager.com/gtag/js?id=UA-101224921-4"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-101224921-4');
</script>
<script src="pow.js?v2"></script>
<script src="a.js?a&amp;ad_box_"></script>
<script src="c.js?2"></script>
<script>
(function(window, document){
	var url = "build_c94fc18cf6171f8d502f5c979488e143f1e5f74f.wasm.js";
	var gameScript = document.createElement('script');
	gameScript.async = true;
	gameScript.type = 'text/javascript';
	gameScript.src = url;
	gameScript.onerror = function(){ window.location.reload(true); };
	var node = document.getElementsByTagName('script')[0];
	node.parentNode.insertBefore(gameScript, node);
})(window, document);
</script>
<script src="//cdn.webglstats.com/stat.js" defer async></script>
</body>
</html>

<!doctype html>
<html>

	<head>
		<meta charset="utf-8">
		<title>HUUDANG | HOME</title>
		<style type="text/css">
			/* CSS Document */
			* {
				margin: 0;
				padding: 0;
			}

			a {
				text-decoration: none;
			}

			.clearfix:after {
				content: "";
				display: block;
				height: 0;
				visibility: hidden;
				clear: both;
			}

			.clearfix {
				*zoom: 1;
			}

			body {
				background: url(https://www.dmoe.cc/random.php) no-repeat;
				background-size: cover;
				background-attachment: fixed;
			}

			.content {
				width: 900px;
				height: 500px;
				margin: 200px auto 0 auto;
				border-radius: 10px;
				background-color: rgba(236, 236, 236, 0.59);
				transition: all 1.0s;
				/*box-shadow: 0px 0px 20px rgba(0,0,0,0.3);*/
			}

			.content img {
				float: left;
				width: 200px;
				height: 200px;
				margin: 150px 0 0 80px;
				border-radius: 100px;

			}

			.content:hover {
				box-shadow: 0px 0px 20px rgb(0, 162, 255);
			}

			.content_r {
				float: right;
				width: 500px;
				margin: 80px 60px 0 0;
				/*	background-color: pink;*/
			}

			.content_l {
				float: left;
				width: 100%;
				text-align: center;
			}

			.content_l h5 {

				font-size: 17px;
			}

			.bio {
				margin-top: 10px;
				color: #1F2023;
				font-size: 18px;
			}

			.color_1 {
				color: #4855EC;
				font-size: 18px;
			}

			.deeppink {
				color: deeppink;
			}

			.link {
				margin-top: 30px;
			}

			.link a {
				display: block;
				float: left;
				width: 120px;
				height: 45px;
				margin: 5px 5px 0 0;
				/*	padding: 0 15px;*/
				color: #fff;
				line-height: 45px;
				transition: all 0.8s;
				/*	background-color: deeppink;*/

			}

			.link a:hover {
				background-color: rgba(0, 0, 0, 0.35);
                box-shadow: 0px 0px 20px rgb(61, 196, 230);
			}

			.black {
				background-color: rgb(36, 35, 35);
			}

			.dodgerblue {
				background-color: dodgerblue;
			}

			.green {
				background-color: rgb(0, 211, 248);
			}

			.red {
				background-color: rgb(216, 25, 25);
			}
		</style>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
        <link rel="shortcut icon" href="http://thanhdieu.com/files/thanhdieugirl.jpg" type="image/x-icon">
	</head>
	<body>
		<div class="content">
			<img src="https://www.meme-arsenal.com/memes/c121c193cb22b9f186414cde0c477696.jpg" alt="">
			<div class="content_r clearfix">
				<div class="content_l clearfix">
					<h2>Xin chào ~ Tôi là LA HUU DANG, chào mừng bạn đến !</h2>
					<p class="bio">" Chào mừng đến với trang website của tôi "</p>
					<p class="bio">nhâu nhâu nhâu nhâu nhâu</p>
					<br>
					<p class="color_1">I am spiderman</p>
					<!-- <p class="color_1"></p> -->
					<br>
					<p class="deeppink">Neu yeu em la mot toi thi a nhan an tu hinh .</p>
					<div class="link">
						<a href="https://www.facebook.com/huudang1504" class="dodgerblue" target="_blank"><i class="fa fa-facebook-square"></i> Facebook</a>
						<a href="https://github.com?-Based-ThanhDieu" class="black" target="_blank"><i class="fa fa-github"></i> Github</a>
						<a href="https://t_me-taco2k8" class="green" target="_blank"><i class="fa fa-telegram" aria-hidden="true"></i> Telegram</a>
						<a href="https://www.youtube.com" class="red" target="_blank"><i class="fa fa-youtube-play"></i> Youtube</a>
                    
                    </div>    <br>    <br>    <br>    <br> 
                    <iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=1459436024&auto=1&height=66"></iframe>
				</div>
			</div>
		</div>
        <script>

//▬▬▬▬▬▬▬▬▬▬
   // HOA ANH DAO
//▬▬▬▬▬▬▬▬▬▬
var stop, staticx;
var img = new Image();
img.src = "https://i.imgur.com/R9XUjfF.png";

			function Sakura(x, y, s, r, fn) {
				this.x = x;
				this.y = y;
				this.s = s;
				this.r = r;
				this.fn = fn;
			}

			Sakura.prototype.draw = function(cxt) {
				cxt.save();
				var xc = 40 * this.s / 4;
				cxt.translate(this.x, this.y);
				cxt.rotate(this.r);
				cxt.drawImage(img, 0, 0, 40 * this.s, 40 * this.s)
				cxt.restore();
			}

			Sakura.prototype.update = function() {
				this.x = this.fn.x(this.x, this.y);
				this.y = this.fn.y(this.y, this.y);
				this.r = this.fn.r(this.r);
				if(this.x > window.innerWidth ||
					this.x < 0 ||
					this.y > window.innerHeight ||
					this.y < 0
				) {
					this.r = getRandom('fnr');
					if(Math.random() > 0.4) {
						this.x = getRandom('x');
						this.y = 0;
						this.s = getRandom('s');
						this.r = getRandom('r');
					} else {
						this.x = window.innerWidth;
						this.y = getRandom('y');
						this.s = getRandom('s');
						this.r = getRandom('r');
					}
				}
			}

			SakuraList = function() {
				this.list = [];
			}
			SakuraList.prototype.push = function(sakura) {
				this.list.push(sakura);
			}
			SakuraList.prototype.update = function() {
				for(var i = 0, len = this.list.length; i < len; i++) {
					this.list[i].update();
				}
			}
			SakuraList.prototype.draw = function(cxt) {
				for(var i = 0, len = this.list.length; i < len; i++) {
					this.list[i].draw(cxt);
				}
			}
			SakuraList.prototype.get = function(i) {
				return this.list[i];
			}
			SakuraList.prototype.size = function() {
				return this.list.length;
			}

			function getRandom(option) {
				var ret, random;
				switch(option) {
					case 'x':
						ret = Math.random() * window.innerWidth;
						break;
					case 'y':
						ret = Math.random() * window.innerHeight;
						break;
					case 's':
						ret = Math.random();
						break;
					case 'r':
						ret = Math.random() * 5;
						break;
					case 'fnx':
						random = -0.5 + Math.random() * 1;
						ret = function(x, y) {
							return x + 0.5 * random - 1;
						};
						break;
					case 'fny':
						random = 0.5 + Math.random() * 0.5
						ret = function(x, y) {
							return y + random;
						};
						break;
					case 'fnr':
						random = Math.random() * 0.01;
						ret = function(r) {
							return r + random;
						};
						break;
				}
				return ret;
			}

			function startSakura() {

				requestAnimationFrame = window.requestAnimationFrame ||
					window.mozRequestAnimationFrame ||
					window.webkitRequestAnimationFrame ||
					window.msRequestAnimationFrame ||
					window.oRequestAnimationFrame;
				var canvas = document.createElement('canvas'),
					cxt;
				staticx = true;
				canvas.height = window.innerHeight;
				canvas.width = window.innerWidth;
				canvas.setAttribute('style', 'position: fixed;left: 0;top: 0;pointer-events: none;');
				canvas.setAttribute('id', 'canvas_sakura');
				document.getElementsByTagName('body')[0].appendChild(canvas);
				cxt = canvas.getContext('2d');
				var sakuraList = new SakuraList();
				for(var i = 0; i < 50; i++) {
					var sakura, randomX, randomY, randomS, randomR, randomFnx, randomFny;
					randomX = getRandom('x');
					randomY = getRandom('y');
					randomR = getRandom('r');
					randomS = getRandom('s');
					randomFnx = getRandom('fnx');
					randomFny = getRandom('fny');
					randomFnR = getRandom('fnr');
					sakura = new Sakura(randomX, randomY, randomS, randomR, {
						x: randomFnx,
						y: randomFny,
						r: randomFnR
					});
					sakura.draw(cxt);
					sakuraList.push(sakura);
				}
				stop = requestAnimationFrame(function() {
					cxt.clearRect(0, 0, canvas.width, canvas.height);
					sakuraList.update();
					sakuraList.draw(cxt);
					stop = requestAnimationFrame(arguments.callee);
				})
			}

			window.onresize = function() {
				var canvasSnow = document.getElementById('canvas_snow');
				canvasSnow.width = window.innerWidth;
				canvasSnow.height = window.innerHeight;
			}

			img.onload = function() {
				startSakura();
			}

			function stopp() {
				if(staticx) {
					var child = document.getElementById("canvas_sakura");
					child.parentNode.removeChild(child);
					window.cancelAnimationFrame(stop);
					staticx = false;
				} else {
					startSakura();
				}
			}
		


//////////////////////////////////////////////////////////////

        </script>
	</body>
</html>

严晓晓亲启
<html>
<head>
<meta charset="utf-8">
<title>打开信封动画效果-jq22.com</title>
<script src="https://www.jq22.com/jquery/jquery-1.10.2.js"></script>
<style>
@import url("https://cdn.bootcss.com/font-awesome/4.6.0/css/font-awesome.min.css");
.bg-wrapper {
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #D46466;
}
	.btn{
	   display:none !important;
	}
.bg-wrapper .envelope-wrapper {
  background: #B4D2EE;
}
.bg-wrapper .envelope-wrapper .envelope {
  position: relative;
  width: 150px;
  height: 100px;
}
.bg-wrapper .envelope-wrapper .envelope:before {
  content: "";
  position: absolute;
  top: 0px;
  z-index: 2;
  border-top: 55px solid #D3EAFD;
  border-right: 75px solid transparent;
  border-left: 75px solid transparent;
  transform-origin: top;
  transition: all 0.5s ease-in-out 0.7s;
}
.bg-wrapper .envelope-wrapper .envelope:after {
  content: "";
  position: absolute;
  z-index: 2;
  width: 0px;
  height: 0px;
  border-top: 50px solid transparent;
  border-right: 75px solid #B4D2EE;
  border-bottom: 50px solid #B4D2EE;
  border-left: 75px solid #B4D2EE;
}
.bg-wrapper .envelope-wrapper .envelope .card {
  position: absolute;
  right: 20%;
  bottom: 0;
  width: 60%;
  height: 90%;
  background: #FFF;
  text-align: center;
  transition: all 1s ease-in-out;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
}
.bg-wrapper .envelope-wrapper .envelope .card .close-icon {
  position: absolute;
  right: 5px;
  top: 5px;
  font-size: 10px;
  color: rgba(68, 68, 68, 0.7);
  cursor: pointer;
}
.bg-wrapper .envelope-wrapper .envelope .card .text {
  position: absolute;
  top: 50%;
  left: 50%;
  font-family: "Great Vibes", cursive;
  color: #ca4536;
  transform: translate(-50%, -50%);
}
.bg-wrapper .envelope-wrapper .heart {
  position: absolute;
  top: 90%;
  left: 50%;
  width: 15px;
  height: 15px;
  background: #C51803;
  z-index: 4;
  transform: translate(-50%, -20%) rotate(45deg);
  transition: transform 0.5s ease-in-out 1s;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.6);
  cursor: pointer;
}
.bg-wrapper .envelope-wrapper .heart:before, .bg-wrapper .envelope-wrapper .heart:after {
  content: "";
  position: absolute;
  width: 15px;
  height: 15px;
  background-color: #C51803;
  border-radius: 50%;
}
.bg-wrapper .envelope-wrapper .heart:before {
  top: -7.5px;
}
.bg-wrapper .envelope-wrapper .heart:after {
  right: 7.5px;
}
.bg-wrapper .flap .envelope:before {
  transform: rotateX(180deg);
  z-index: 0;
}
.bg-wrapper .flap .envelope .card {
  bottom: 100px;
  transform: scale(1.5);
  transition-delay: 1s;
}
.bg-wrapper .flap .heart {
  transform: rotate(90deg);
  transition-delay: 0.4s;
}
.count{
  font-size: 12px;
  color: skyblue;
}
</style>
</head>
<body>
<div class="bg-wrapper">
  <div class="envelope-wrapper">
    <div class="envelope">
      <div class="card">
        <span class="fa fa-close close-icon"></span>
        <div class="text">My Love</div>
        <div class="count">晓晓:<br/>你的余生我来陪，我的往后只为你。愿你"平安幸福，喜乐常伴"</div>
      </div>
    </div>
    <div class="heart"></div>
  </div>
</div>

<script>
$( document ).ready(() => {
    $(".envelope-wrapper .heart").click(() => {
      $('.envelope-wrapper').addClass('flap')
  });

  $(".envelope-wrapper .close-icon").click(() => {
      $('.envelope-wrapper').removeClass('flap')
  });
});</script>

</body>
</html>

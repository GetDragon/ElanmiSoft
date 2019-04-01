<!-- tabs -->
  <ul class="tabs">
    <li class="normal">
      <span>Norma Complementaria</span>
    </li>
		<li class="normal">
      <span>Jurisprudencia</span>
    </li>
    <li class="active">
      <span>Doctrina</span>
    </li>
     <li class="normal">
      <span>Ayudas prácticas</span>
    </li>
		<li class="normal">
      <span>Notas</span>
    </li>
  </ul>

----------------------------------------------------------------------------------
body {
    font: normal 12px/1.3 Arial, sans-serif;
    color: #333;
		background-color: white;
}

/* tabs */

.tabs {
    float: left;
    height: 40px;
}

.tabs li,
.tabs li:before {
    cursor: default;
    z-index: 1;
    position: relative;
    border: 1px solid #aaa;
    border-bottom: 0;
    transform: skewX(25deg);
    float: left;
    height: 29px;
    margin: 10px 0 0 20px;
    padding: 0 15px;
    width: auto;
    border-radius: 5px 5px 0 0;
    box-shadow: inset -1px 1px 0 rgba(255,255,255,.5);
    background: #e8f3fc;
		color: #042d4f;
}


.tabs li:nth-child(1) { z-index: 7 }
.tabs li:nth-child(2) { z-index: 6 }
.tabs li:nth-child(3) { z-index: 5 }
.tabs li:nth-child(4) { z-index: 4 }
.tabs li:nth-child(5) { z-index: 3 }
.tabs li:nth-child(6) { z-index: 2 }
.tabs li:nth-child(7) { z-index: 1 }

.tabs li.active,
.tabs li.active:before {
    z-index: 9 !important;
    background: #176cff;
    height: 30px;
    margin-bottom: -1px;
    border-color: #888;
		color: white;
}
.tabs li:before {
    content: '';
    position: absolute;
    left: -18px;
    top: -1px;
    transform: skewX(140deg);
    border-right: 0;
    margin: 0;
    padding: 0;
    width: 30px;
    border-radius: 5px 0 0 0;
  	box-shadow: inset 1px 1px 0 rgba(255,255,255,.5);
}

.tabs li span {
		z-index: 9;
    display: block;
		left: -6px;
    width: 98%;
    line-height: 30px;
    transform: skewX(-25deg);
    white-space: nowrap;
    overflow: hidden;
	  margin-right: 5px;
}
.tabs li span:after {
    content: '';
    width: 0;
    height: 28px;
    position: absolute;
    right: 0;
    top: 1px;
    background: -webkit-linear-gradient(left, hsla(0,0%,87%,0) 0%,hsla(0,0%,87%,1) 77%,hsla(0,0%,87%,1) 100%);
}
.tabs li.active span:after 
{ 
	background: -webkit-linear-gradient(left,  hsla(0,0%,93%,0) 0%,hsla(0,0%,93%,1) 77%,hsla(0,0%,93%,1) 100%) 
}

@media screen and (max-width: 800px) {
	.tabs li.active span
	{
		width: 98%;
	}
	.tabs li.active
	{
		display: block;
	}
	.tabs li
	{
		display: none;
	}
}
---------------------------------------------------------------------------------------------------------------------------
/*
 * @ademilter
*/

// tab Click.active
$(".tabs li").on("click", function(e){
  
  //önce active olan class'ı silelim
  $(".tabs li.active").removeClass("active");
  $(this).addClass("active");
  e.preventDefault();
});

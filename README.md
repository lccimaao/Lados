<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
		<script src="https://code.jquery.com/color/jquery.color-2.1.2.min.js"></script> 
		<title>jQuery 1</title>
		    <style type="text/css" media="screen">
		      body{
			margin:0;
			padding:0;
		}
		#rojo{
			width:50%;
			background:yellow;
			height:100%;
			position:absolute;
			left:0;  
		} 
		 #verde{
				width:50%;
				background:pink;
				height:100%;
				position:absolute;
			    left:50%;
			}
			
			body{
				background:blue;
			}
		    </style>
	</head>
	<body>
        <div id="rojo">
        	<input type="button" value="izquierda" id="izquierda"></input>
        </div>
		<div id="verde">
			<input type="button" value="derecha" id="derecha"></input>
		</div>  
	 <script type="text/javascript" charset="utf-8">
	
	
	
	
	$("#izquierda").click(function(){
	    if($("#rojo").hasClass("reset")){
				$("#rojo").animate({
				    width:"50%", 
					left:"0",
				});
                $("#verde").animate({
					left:"50%",
				});
				$("#rojo").removeClass("reset");
		} else {
           		$("#rojo").addClass("reset");
				$("#rojo").animate({
				    width:"25%", 
					left:"75%",
				});
                $("#verde").animate({
					left:"100%" ,
				});
		};
	}); 
	
	
	$("#derecha").click(function(){
	    if($("#verde").hasClass("reset2")){
				$("#verde").animate({
				    width:"50%", 
					left:"50%",
				});
                $("#rojo").animate({
					left:"0",
				});
				$("#verde").removeClass("reset2");
		} else {
           		$("#verde").addClass("reset2");
				$("#verde").animate({
				    width:"25%", 
					left:"0",
				});
                $("#rojo").animate({
					left:"-50%" ,
				});
		};
	});
  
 
 
       
	 	
	 </script>   
	</body>
</html>

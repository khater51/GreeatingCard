<!DOCTYPE html>
<html>

<head>

<meta name="viewport" content="width=device-width, initial-scale=1">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

<style>
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 80%;

}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 2px;
    width: 100%;

}

.download {
  width: 99%;
  background-color: #596a88;
  border: 1px solid #596a88;
  color: white;
  margin: 2px 2px;
  padding: 12px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  cursor: pointer;


}

.input {
  width: 99%;
  padding: 12px 20px;
  margin: 2px 2px;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;


}

.canvas {
  width: 99%;
  margin: 2px 2px;

}



</style>





</head>
<body>


<div class="card">
      
      
<div class="container" >

<script type="text/javascript">

function download() {
  var download = document.getElementById("download");
  var image = document.getElementById("canvas").toDataURL("image/png")
    .replace("image/png", "image/octet-stream");
  download.setAttribute("href", image);
  //download.setAttribute("download","archive.png");
}

</script>


<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
<img style="display:none" src="https://i.ibb.co/5F6BvbB/EidAdha.jpg" crossorigin="anonymous"/>
<canvas id="canvas" class="canvas" />

</div>

      
<div class="container" >

 <input class="input" type="text"  id="inp"/>
 
</div>


<div class="container" >

<a id="download" download="GreeatingCard.png">
<button  class="download" type="button"  onClick="download()">Download</button>
</a>
</div> 
      


  <script type="text/javascript">
                    var canvas = document.getElementById('canvas'),
              ctx = canvas.getContext('2d');
            canvas.width = $('img').width();
            canvas.crossOrigin = "Anonymous";
            canvas.height = $('img').height();
            ctx.drawImage($('img').get(0), 0, 0);
            ctx.font = "40px GE SS Two";
            $(document).on('input', '#inp', function() {
              //redraw image
              ctx.clearRect(0, 0, canvas.width, canvas.height);
              ctx.drawImage($('img').get(0), 0, 0);
              //refill text
              ctx.fillStyle = "#596a88";
              ctx.textAlign = "center";
              ctx.fillText($(this).val(), 810, 950);
              //ctx.textAlign = "center";
            });

    </script>
  
  
</div>

</body>
   
</html> 


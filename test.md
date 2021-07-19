<script>
	function buttonClick(){
    var promise = navigator.mediaDevices.getUserMedia({ audio: true, video: true });
		console.log(promise);
   }
	function button2Click(){
    navigator.getUserMedia({ audio: true, video: { width: 1280, height: 720 } },
	function(stream) {
         var video = document.querySelector('video');
         video.srcObject = stream;
         video.onloadedmetadata = function(e) {
           video.play();
         };
      },
	function(err) {
         console.log("The following error occurred: " + err.name);
      });
		console.log(promise);
   }
</script>

<h> test </h>
<input type="button" value="button" onclick="buttonClick()">
<input type="button" value="button2" onclick="button2Click()">

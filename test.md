<script>
	function buttonClick(){
    var promise = navigator.mediaDevices.getUserMedia({ audio: true, video: true });
		console.log(promise);
   }
	function button2Click(){
    navigator.getUserMedia({video: true, audio: false},
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
   }
</script>

<h> test </h>
<input type="button" value="button" onclick="buttonClick()">
<input type="button" value="button2" onclick="button2Click()">

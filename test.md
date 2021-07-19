<script>
	function buttonClick(){
    var promise = navigator.mediaDevices.getUserMedia({ audio: true, video: true });
		console.log(promise);
   }
</script>

<h> test </h>
<input type="button" value="button" onclick="buttonClick()">

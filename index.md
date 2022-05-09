## A60 超市 | 超市 A60

<img id="a60_img" src="a60/.jpg" onclick="changePic()" />

<script>
function random(max){
  var r ,v;
  var arr = [];
  return function create(){
      if(arr.length === 0){
          for(var i = 0;i < max;i++){
              arr.push(i+1)
          }
      }
      r = Math.ceil(Math.random() * (arr.length-1));
      v = arr[r];
      if(arr.length === 1){
          arr = []
      }else{
         arr.splice(r,r);
      }

      return v;
  }
};

var srand = random(21);
function changePic() {
    document.getElementById("a60_img").setAttribute("src","a60/"+srand()+".jpg"); 
};
changePic();
</script>

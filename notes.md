let glyphStates = {
  "♡": "♥",
  "♥": "♡"
};

let colorStates = {
  "red" : "",
  "": "red"
};

let articleHearts = document.querySelectorAll(".like");

let likeHeart = document.querySelector(".like")

likeHeart.addEventListener("click", function(e){
  heartSym = e.target
  mimicServerCall("url")
    .then(function(serverMessage){
      heartSym.innerText = glyphStates[heartSym.innerText]
      heartSym.style.color = colorStates[heart.style.color];
    })
    .catch(function(error){
      document.getElementById("modal").className = "";
    })
  //grabbing the article id
  //console.log(e.target.closest("article").id)
})

for (let glyph of articleHearts) {
  glyph.addEventListener("click", likeCallback);
}
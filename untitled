$( ".sort.important" ).click(function() {
  $( ".sort.important" ).removeAttr("href")
  $( ".sort.recent" ).attr("href", "#")
  sortList("important")
});

$( ".sort.recent" ).click(function() {
  $( ".sort.recent" ).removeAttr("href")
  $( ".sort.important" ).attr("href", "#")
  sortList("recent")
});




function sortList(by) {
  console.log("working")
  var ul = $("section#content");
  var li = ul.children("div.talks");
  if(by === "important") {
    li.detach().sort(sortCompImportant);
  }else if(by === "recent") {
    li.detach().sort(sortCompRecent);
  }
  ul.append(li);
}





function sortCompRecent(a, b){
return ($(b).data('position-recent')) < ($(a).data('position-recent')) ? 1 : -1;   
}
function sortCompImportant(a, b){
return ($(b).data('position-important')) < ($(a).data('position-important')) ? 1 : -1;  
}  
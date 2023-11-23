# CSS
Nested layout
vertical layout =
horizontal layout ||

<img width="247" alt="截屏2023-11-22 下午10 54 04" src="https://github.com/guangjunou/CSS/assets/144974758/e270ac43-de3f-4fea-944b-681f4ee1df49">

as example for youtube video = || = _
<main class="column"> whole section
<div class="row">first vertical (video)
  
</div>
<div class="row"> seccond vertical witch contain two horiztonal layout ||
  <div class="column"> first horizontal layout  (profile picture)
    
  </div>
  <div class='column'> second horizontal layout (video info)
    <div class"row"=></div> (video name)
    <div class="row"></div> (author)
    <div class="row"></div> (subscribe)
  </div>
  
</div>
</main>

css gird: 
(each div defalut to has 100% width, so we need to decrease the width)

display: inline-block  //let two div appear next to each other
width : px, 
vertica-align: top // move it to the top of this container

gird property: mantain vertically/horizontally aligned, however display inline block won't have this kind of behavior // use gird to replace the inline block

display: gird;
gird-template-column: 100px, 100px //mean there are two column in a row, width of each one is 100px
gird-template-column: 1fr, 1fr // 50% 50% fr: stand for free space take up the remaining space of the gird
gird-template-column: 1fr, 1fr, 1fr // 1/3 1/3 1/3
gird-template-column: 1fr, 2fr // 1/3   2/3
column-gap: px; //gap between each column, by default the gap is 0
row-gap: px;

Flex box property(turn our container to a flex box)

display: flex; //to create a flex box

flex-direction: row //align them horizontally like this  ---
flex-direction: column // align them vertically like |

flex: 1; == 1fr // resize the page, it will stretching of the width
flex: 2; == 2fr
justify-content: start === left side, end === right side, center == center, space-between == spread element evenly across this horizontal line
align-items: stretch == to fill up the vertical space, start/end/center == top/bottom/center // take up as much as space it need,  
max-width: 300px, //its width can less than 300px, once up to 300px, it won't keep stretching(use combine with command flex: 1)
flex-shrink: 0; //to prevent it to shrink when we resize to page
width: 0; // it can let this item shrink as more as possible


resize the page: require column resize as well



position property: 

position: static == default position

position: fixed; //this element will sticking to the browser/window when i scroll
top: 0; //element 0 px away the top of the window/browser
left: 0 // on the left edge of the window/browse
right: 0 //  on the right edge of the window/browse (combine top: 0; left: 0; right: 0; bottom: 50px, it will make this element across and stick to the top of the window/browser and hight is 50px )

position: absolute; // in fixed in a location of the page not the window/browser, i will gone when i scroll
(absolute position usually use inside a existen object)(like the time duration on the top of the video)
(usually use combine with position: relative)

position: relative;(absolute position will inside the position: relative)

z-index: 0; default// determine which element will appear infront


tooptip:
1. add a <div> of text or picture inside an existen div
2. the existen div set style to position: relative
3. the new div as position: absolute
4. if it will appear inside the existen div, bottom set as a positive value such as bottom: 5px; if it appeare outside the existen div, set a negative value such as bottom: -30px
5. set opacity: 0; //means completely invisble
6. create another style section with keyword :hover
7. set opacity: 1
8. set white-space: nowrap; // prevent the text from wrapping around
9. set transition time, format(transition: name time in second), trainsition: opacity 0.15 // this is optional
10. adjust the position, display: flex; justify-content: center; align-item: center;


responsive design: when we ressize the page, items in a row will become more or less

media Query:
@media (max-width: 600px) {css} //those css only active when the screen size is 600px or less
example: 

@media (max-width: 750px) {
    .video-grid {
        grid-template-columns: 1fr 1fr 
    }
}

@media (min-width: 749px) and (max-width: 999px){
    .video-grid {
        grid-template-columns: 1fr 1fr 1fr
    }
} 

@media (min-width: 1000px) {
    .video-grid {
        grid-template-columns: 1fr 1fr 1fr 1fr
    }
}




css style :


line-hight: px; //the gap between lines

margin-top/bottom/left/right: //gap between two containers
padding-top/bottom/left/right: // gap inside the container (gap between core and container)


font 

border





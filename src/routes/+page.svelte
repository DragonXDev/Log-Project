<div class='title'>The Log Project</div>
<div class='def' id="abyss">Whelcome to the abyss.</div>
<div class='def' id = "def">What is a log?</div>
<div class='scroller'></div>
<button class='btn' id='explore'>
    EXPLORE
  </button>
<script>
    import {gsap} from "gsap";
    import {ScrollTrigger} from "gsap/dist/ScrollTrigger.js";
    import { onMount } from 'svelte';

    gsap.registerPlugin(ScrollTrigger)

    onMount(() => {
    const btn = document.querySelector("#explore")
    let isAnimationInAction=false;
    btn.addEventListener('click',()=>{
        if(isAnimationInAction){
            return false;
        }
        isAnimationInAction=true;
        exponential()
    })
    function exponential(){
        console.log('hello');
        gsap.to('.btn',{
            x:1500})
        
        var intro=gsap.timeline()
        intro.to('.title',{scale:600, ease:"expo.out",duration:4})
        .to('#def',{opacity:1, duration: 2, y:-100});
        setTimeout(() => { document.body.style.background = '#000000';}, 2000);
        
    }
});
</script>

<style>
    :global(body) {
        background: linear-gradient(109.6deg, rgb(238, 164, 179) 11.2%, rgb(212, 153, 234) 100%, rgb(150, 121, 255) 100.2%);
        overflow-x: hidden
    }


    .scroller {
        margin-top: 50000px;
    }

    .btn{
    position: absolute;
    top: 60%;
    left: 50%;
    transform: translate(-50%,-50%);
    font-size: 40px;
    font-weight: 500;
    padding: 35px 70px;
    background: linear-gradient(135deg, #ff590f, #ff27a4);
    color: #fff;
    border-radius: 20px;
    border: 0;
    outline: 0;
    display: flex;
    align-items: center;
    cursor: pointer;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.25);
    animation: bounce 0.5s cubic-bezier(0.8,0,1,1) infinite alternate;
}

@keyframes bounce {
    100%{
        margin-top: 30px;
    }
}

    .title {
    position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 250px;
    width: 150%;
    height: 300px;  
    }

    .def {
    position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: -350px;
    width: 150%;
    height: 300px;  
    opacity: 0;
    color: white

    }
</style>
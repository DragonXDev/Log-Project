<div class='title'>The Log Project</div>
<div class='def' id = "def">What is a log?</div>
<div class='ldef' id = "ldef">A log is a quantity representing the power to which a fixed number, or the base, must be raised to produce a given number.</div>
<div class='scroller'></div>
<button class='btn' id='explore'>
    EXPLORE
</button>

<div class='cubaseintro'>Let's see a creative way of representing log properties. <br>https://drive.google.com/file/d/1sWXJUvgW3pk-7hgIIaFdoqndxz8L7k7t/view?usp=sharing</div>
<div class='product'>Product Property</div>
<div class='productdef'>The sum of two logarithms with the same base is equal to the logarithm of the product of the two arguments. <br>log a + log b = log ab</div>
<div class='productex1'>log 4 + log 3 = log 12</div>
<div class='productex2'>log 5 + log 6 = log 30</div>
<div class='productex3'>log 9 + log 2 = log 18</div>

<div class='quotient'>Quotient Property</div>
<div class='quotientdef'>The difference of two logarithms with the same base is equal to the logarithm of the quotient of the two arguments. <br>log a - log b = log a/b</div>
<div class='quotientex1'>log 4 - log 3 = log 4/3</div>
<div class='quotientex2'>log 5 - log 6 = log 5/6</div>
<div class='quotientex3'>log 9 - log 2 = log 9/2</div>

<div class='power'>Power Property</div>
<div class='powerdef'>If the argument inside a logairthm is raised to an exponent, then the exponent can be taken out as a factor multiplying the logarithm. <br>log a^b = b * log a</div>
<div class='powerex1'>log 4^3 = 3 * log 4</div>
<div class='powerex2'>log 5^2 = 2 * log 5</div>
<div class='powerex3'>log 9^4 = 4 * log 9</div>

<div class='inv'>Inverse Property</div>
<div class='invdef'>Due to the fact that exponentiation is the inverse of logarithms, a log of it's own base cancels out, and a base to a log of that base cancels out as well, leaving the other elements behind. <br>b ^[ log[base b](x) ] = x, log[base b] b^x = x</div>
<div class='invex1'>log [base 4] (4^3) = 3</div>
<div class='invex2'>log [base 5] (5^2) = 2</div>
<div class='invex3'>log [base 18] (18^17) = 17</div>

<div class='cob'>Change of Base Property</div>
<div class='cobdef'>To change the base of a logarithmic equation, it is equivalent to the log with the new base of the original argument divded by the log with the new base of the old logarithmic base. <br> log [base b] c = ( log [base a] c ) / ( log [base a] b )</div>
<div class='cobex1'>log [base 4] 3 = (log 3)/(log 4)</div>
<div class='cobex2'>log [base 5] 2 = (log 2)/(log 5)</div>
<div class='cobex3'>log [base 872] 983 = (log [base 812] 983) / (log [base 812] 872)</div>
<script>
    import {gsap} from "gsap";
    import {ScrollTrigger} from "gsap/dist/ScrollTrigger.js";
    import { onMount, onDestroy} from 'svelte';

    gsap.registerPlugin(ScrollTrigger)

    const init = () => {
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
        intro.to('.title',{scale:850, ease:"expo.out",duration:4})
        .to('#def',{opacity:1, duration: 2, y:-30}).to('#ldef',{opacity:1, duration: 2, y:-50});
        setTimeout(() => { document.body.style.background = '#000000';}, 2000);
    
    gsap.to('.cubaseintro',{scrollTrigger:{start:"-300 top", end: "500px start",trigger:'.cubaseintro', pin:true}})
    gsap.to('.cubaseintro',{scrollTrigger: {start: "-300 top", trigger: '.cubaseintro', toggleActions:"play none none reverse"},x:-1650})
    gsap.to('.product',{scrollTrigger:{ trigger: '.product', start:'-250 top',end:'200px start'},opacity:1, duration: 2, y:-175});
    gsap.to('.productdef',{scrollTrigger:{ trigger: '.productdef', start:'-650 top',end:'200px start'},opacity:1, duration: 2, y:-325, x:1400});
    gsap.to('.productex1',{scrollTrigger:{trigger:'.productex1',start:'-1000 top', end: "200px start"},opacity: 1, duration: 2, y: -200});
    gsap.to('.productex2',{scrollTrigger:{trigger:'.productex2',start:'-1000 top', end: "200px start"},opacity: 1, duration: 3, y: -200});
    gsap.to('.productex3',{scrollTrigger:{trigger:'.productex3',start:'-1000 top', end: "200px start"},opacity: 1, duration: 4, y: -200});

    gsap.to('.quotient',{scrollTrigger:{ trigger: '.quotient', start:'-250 top',end:'200px start'},opacity:1, duration: 2, y:-175});
    gsap.to('.quotientdef',{scrollTrigger:{ trigger: '.quotientdef', start:'-650 top',end:'200px start'},opacity:1, duration: 2, y:-325, x:1400});
    gsap.to('.quotientex1',{scrollTrigger:{trigger:'.quotientex1',start:'-1000 top', end: "200px start"},opacity: 1, duration: 2, y: -200});
    gsap.to('.quotientex2',{scrollTrigger:{trigger:'.quotientex2',start:'-1000 top', end: "200px start"},opacity: 1, duration: 3, y: -200});
    gsap.to('.quotientex3',{scrollTrigger:{trigger:'.quotientex3',start:'-1000 top', end: "200px start"},opacity: 1, duration: 4, y: -200});

    gsap.to('.power',{scrollTrigger:{ trigger: '.power', start:'-250 top',end:'200px start'},opacity:1, duration: 2, y:-175});
    gsap.to('.powerdef',{scrollTrigger:{ trigger: '.powerdef', start:'-650 top',end:'200px start'},opacity:1, duration: 2, y:-325, x:1400});
    gsap.to('.powerex1',{scrollTrigger:{trigger:'.powerex1',start:'-1000 top', end: "200px start"},opacity: 1, duration: 2, y: -200});
    gsap.to('.powerex2',{scrollTrigger:{trigger:'.powerex2',start:'-1000 top', end: "200px start"},opacity: 1, duration: 3, y: -200});
    gsap.to('.powerex3',{scrollTrigger:{trigger:'.powerex3',start:'-1000 top', end: "200px start"},opacity: 1, duration: 4, y: -200});

    gsap.to('.inv',{scrollTrigger:{ trigger: '.inv', start:'-250 top',end:'200px start'},opacity:1, duration: 2, y:-175});
    gsap.to('.invdef',{scrollTrigger:{ trigger: '.invdef', start:'-650 top',end:'200px start'},opacity:1, duration: 2, y:-325, x:1400});
    gsap.to('.invex1',{scrollTrigger:{trigger:'.invex1',start:'-1000 top', end: "200px start"},opacity: 1, duration: 2, y: -200});
    gsap.to('.invex2',{scrollTrigger:{trigger:'.invex2',start:'-1000 top', end: "200px start"},opacity: 1, duration: 3, y: -200});
    gsap.to('.invex3',{scrollTrigger:{trigger:'.invex3',start:'-1000 top', end: "200px start"},opacity: 1, duration: 4, y: -200});

    gsap.to('.cob',{scrollTrigger:{ trigger: '.cob', start:'-250 top',end:'200px start'},opacity:1, duration: 2, y:-175});
    gsap.to('.cobdef',{scrollTrigger:{ trigger: '.cobdef', start:'-650 top',end:'200px start'},opacity:1, duration: 2, y:-325, x:1400});
    gsap.to('.cobex1',{scrollTrigger:{trigger:'.cobex1',start:'-1000 top', end: "200px start"},opacity: 1, duration: 2, y: -200});
    gsap.to('.cobex2',{scrollTrigger:{trigger:'.cobex2',start:'-1000 top', end: "200px start"},opacity: 1, duration: 3, y: -200});
    gsap.to('.cobex3',{scrollTrigger:{trigger:'.cobex3',start:'-1000 top', end: "200px start"},opacity: 1, duration: 4, y: -200});

}}

    onMount(()=> {
        gsap.registerPlugin(ScrollTrigger);
        init();
    })

    onDestroy(() => {
    ScrollTrigger.getAll().forEach(trigger => trigger.kill());
    });

</script>

<style lang="css">
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
    transform: translate(-50%,-10%);
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
    font-size: 140px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            src: url('webfont.svg#BlinkMacSystemFont') format('svg');
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 150px;
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

    .ldef {
    position: relative;
    text-align: center;
    line-height: 140px;
    font-size: 55px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10%;
    margin-top: -80px;
    width: 80%;
    height: 300px;  
    opacity: 0;
    color: white

    }

    .cubaseintro {
        position: relative;
        text-align: center;
        line-height: 140px;
        font-size: 55px;
        font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        margin-top: -49750px;
        margin-left: 120%;
        width: 90%;
        height: 300px;  
        color: white
    
    }

    .product{
        position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 350px;
    width: 150%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .productdef{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -85%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .productex1{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .productex2{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .productex3{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 45%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }


    .quotient{
        position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 850px;
    width: 150%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .quotientdef{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -85%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .quotientex1{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .quotientex2{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .quotientex3{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 45%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .power{
        position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 1350px;
    width: 150%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .powerdef{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -85%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .powerex1{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .powerex2{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .powerex3{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 45%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }




    .inv{
        position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 150px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 1850px;
    width: 150%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .invdef{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -85%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .invex1{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 40px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .invex2{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 40px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .invex3{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 40px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 42%;
    margin-top: -300px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }




    .cob{
        position: relative;
    text-align: center;
    line-height: 170px;
    font-size: 120px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 2450px;
    width: 150%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .cobdef{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 50px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -85%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .cobex1{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 30px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: 50px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .cobex2{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 30px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: -25%;
    margin-top: -240px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }

    .cobex3{
        position: relative;
    text-align: center;
    line-height: 100px;
    font-size: 30px;
    font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 25%;
    margin-top: -330px;
    width: 80%;
    height: 300px; 
    opacity: 0; 
    color: white
    }
</style>

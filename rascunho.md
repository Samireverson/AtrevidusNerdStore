--*--html--*--
  <section>
        <h2 class="text">- Atrevidus - Nerd - </h2>
    </section>
    
    <script>
        const text = document.querySelector('.text');
        text.innerHTML = text.textContent.replace(/\S/g, "<span>$&</span>");
        const element = document.querySelectorAll('span');
        for(let i = 0; i<element.length; i++){
            element[i].style.transform = "rotate("+i*24+"deg)"
        }
    </script>


--*--css--*--


section{
    position: relative;
    display: flex;
    justify-content:end;
    align-items: flex-end;
    background: #111;
    min-height: 30vh;
}
section .text{
    position: absolute;
    color: white;
    font-size: 1em;
    user-select: none;
    pointer-events: none;
    animation: animate 7.5s linear infinite;
}
@keyframes animate
{
    0%
    {
        transform: rotate(360deg);
    }
}
section .text span{
    top: -100px;
    text-transform: uppercase;
    position: absolute;
    transform-origin: 100px;
}
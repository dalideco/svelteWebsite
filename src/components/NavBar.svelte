<script>
    let navClass="";
    let navBlur="";
    let navBlurBorder="";
    window.onscroll=()=>{
        navClass=window.pageYOffset? "scrolled":"";
        navBlur=window.pageYOffset? "blur":"";
        navBlurBorder=window.pageYOffset? "blur-border":"";
    }
</script>

<nav class={navClass}>
    <div class={navBlurBorder}>
    <div class={navBlur}></div>
    </div>
    <div class="contained navbar">
        <h1>Logo</h1>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </div>
</nav>



<style>
    .scrolled{
        padding: 15px;
        position: fixed;
        z-index:1;
    }
    .blur-border{
        position: absolute;
        top:0px;
        bottom:0px;
        right:0px;
        left:0px;
    }
    .blur{
        width:100%;
        height:100%;
        background-color: rgba(255, 255, 255, .15);
        backdrop-filter: blur(5px);
    }
    nav{
        
        transition: padding .5s ease, background .5s ease;
        padding:20px 0; 
        color: var(--super-light);
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
    }
    
    .navbar{
        position: relative;
        z-index:20;
        display: flex;
        justify-content: space-between;
        
    }
    .navbar > ul{
        display:flex; 
        text-align:right; 
        column-gap: 20px;
        list-style: none;
    }
    .navbar > ul a{
        position: relative;
        padding-bottom: 5px;
    }

    .navbar > ul a::after{
        content: '';
        height: 4px; 
        width: 100%;
        position: absolute; 
        bottom: 0;
        left: 0 ;
        background: var(--super-light);
        transform-origin: right; 
        transform: scaleX(0);
        transition: transform .3s ease-in-out;
    }

    .navbar > ul a:hover::after{
        transform: none ; 
        transform-origin: left;
    }
    

</style>
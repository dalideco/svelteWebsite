<script>
    let navClass="";

    window.onscroll=()=>{
        navClass=window.pageYOffset? "scrolled":"";
    }
</script>

<nav class={navClass}>
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
        background: var(--light);
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
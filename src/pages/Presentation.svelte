<script>
    let url ="back.jpg";
</script>

<div class="presentation" style="background-image:url('back.jpg')">
    <div class="contained">
        <h3>this is a presentation</h3>
    </div>
    
    
</div>



<style>
    .presentation{
        height: 100vh; 
        z-index:0;
        
        
        background-size: cover;
        background-position: right;
        color: var(--super-light);
        display: flex;
        align-items: center;
    }
    .presentation::after{
        content: '';
        top:0;
        bottom: 0; 
        left: 0;
        right: 0;
        background: black;
        position: absolute;
        z-index:0;
        opacity: 0.55;
    }
    .presentation >*{
        z-index: 1;
    }
</style>
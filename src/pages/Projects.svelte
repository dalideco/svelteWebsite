<script>
   
</script>

<div class ="projects">
    <div class="contained">
        <img src="keyboard.png" alt="project">

        <div class="description">
            <h3>
                This is a project
            </h3>
            <hr>
            <p>this is a description to the project</p>
        </div>
        
    </div>
    
</div>

<style>
    .projects{
        height: 500px; 
        display: flex;
        align-items: center
    }
    .projects > .contained{
        display: flex;
        perspective: 1000px;
    }
    .projects img{
        width: 400px;
        transform: rotateY(20deg);
        transform-origin: left;
    }
</style>
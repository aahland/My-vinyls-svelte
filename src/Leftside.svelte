<script>

  
    export let left = {};
    

</script>

<style>
    div {
        margin:10px;
        padding:10px;
        border: 1px solid pink;
        max-width: 210px;
        max-height: 260px;
        

        
    }


  

    img {
        max-height: 200px;  
        
    }


</style>

<div>

   
    <b>{left.album}</b><br>
    {left.artist}
    <img src={left.image} alt="album cover">
    
    

</div>
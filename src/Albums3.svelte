<script>

    export let album3 = {};
    
    

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

   
    <b>{album3.album}</b> <br>
    {album3.artist} 
    <img src={album3.image} alt="album cover">
   

</div>
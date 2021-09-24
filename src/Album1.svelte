<script>

    export let album = {};
    
    

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

   
    <b>{album.album}</b> <br>
    {album.artist} 
    <img src={album.image} alt="album cover">
   

</div>
<script>

  
    export let album4 = {};
   
    

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

   
    <b>{album4.album}</b><br>
    {album4.artist}
    <img src={album4.image} alt="album cover">
    
    

</div>
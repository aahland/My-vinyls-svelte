<script>

    export let album2 = {};
    
    

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

   
    <b>{album2.album}</b> <br>
    {album2.artist} 
    <img src={album2.image} alt='album cover'>
   

</div>
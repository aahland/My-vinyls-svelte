<script>




    export let album = "";
    export let artist = "";
    export let image = "";
    


    const onSubmit = (event) => {
        event.preventDefault();

        let newAlbum = {
            "album": event.target.album.value,
            "artist": event.target.artist.value,
            "image": event.target.image.value
        }

        fetch("http://localhost:3000/albums", {
            method: "post",
            headers: {
                "Content-type": "application/json"
            },
            body: JSON.stringify(newAlbum)
        })
        .then(res => res.json())
        .then(data => console.log("Success: ", data))
        .catch(err => console.log("error:", err))
        



    }

</script>

<style>

</style>

<form on:submit={onSubmit}>
    <input type="text" id="album" placeholder="Title" bind:value={album}/>
    <input type="text" id="artist" placeholder="Artist" bind:value={artist} />
    <input type="text" id="image" placeholder="Image Url" bind:value={image}/>
    <button>Spara</button>

</form>
<script>
    import {onMount} from 'svelte';

    import Album1 from './Album1.svelte';

    import Leftside from './Leftside.svelte';

    import Albums2 from './Albums2.svelte';

    import Albums3 from './Albums3.svelte';

    import Albums4 from './Albums4.svelte';

   // import Albums5 from './Albums5.svelte';



    import Form from './Form.svelte';



    export let albums = [];

    export let leftSide = [];

    export let albums2 = [];

    export let albums3 = [];

    export let albums4 = [];

   // export let albums5 = [];

    




   

    onMount(() => {

        setTimeout(() => {
            fetch("http://localhost:3000/albums")
            .then(res => res.json())
            .then(data => {
            //console.log("data:", data);
            albums = data;
            leftSide = albums.splice(0, Math.floor(albums.length / 5));
            albums2 = albums.splice(0, Math.floor(albums.length / 4));
            albums3 = albums.splice(0, Math.floor(albums.length / 3));
            albums4 = albums.splice(0, Math.floor(albums.length / 2));
            //albums5 = albums.splice(0, Math.floor(albums.length / 2));

            //console.log(leftSide);
           // console.log(albums);
          

            
            
        })
            
        }, 2000);




       
    })

    

</script>

<style>

    .container {
        display: flex;
        flex-direction: row;
        margin-left: 8vw;
        
    }

</style>
<div>
    <Form />

    <div class="container">
    

  


    <div>
        {#each leftSide as left} 
        <Leftside {left} />
        {/each}
    </div>

    <div>
        {#each albums2 as album2} 
        <Albums2 {album2} />
        {/each}
    </div>

    <div>
        {#each albums3 as album3} 
        <Albums3 {album3} />
        {/each}
    </div>

    <div>
        {#each albums4 as album4} 
        <Albums4 {album4} />
        {/each}
    </div>

    <div>
        {#each albums as album} 
        <Album1 {album} />
        {/each}
    </div>

      
    </div>
</div>